An HTML Form is a group of one or more fields/widgets on a web page, which can be used to collect information from users for submission to a server. Forms are a flexible mechanism for collecting user input because there are suitable widgets for entering many different types of data, including text boxes, checkboxes, radio buttons, date pickers and so on. Forms are also a relatively secure way of sharing data with the server, as they allow us to send data in POST requests with cross-site request forgery protection.

The submit input will be displayed as a button by default. This can be pressed to upload the data in all the other input elements in the form to the server (in this case, just the team_name field). The form attributes define the HTTP method used to send the data and the destination of the data on the server (action):

action: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL.
method: The HTTP method used to send the data: post or get.
The POST method should always be used if the data is going to result in a change to the server's database, because it can be made more resistant to cross-site forgery request attacks.
The GET method should only be used for forms that don't change user data (for example, a search form). It is recommended for when you want to be able to bookmark or share the URL.


# the main things that Django's form handling does are:

Display the default form the first time it is requested by the user.
The form may contain blank fields if you're creating a new record, or it may be pre-populated with initial values (for example, if you are changing a record, or have useful default initial values).
The form is referred to as unbound at this point, because it isn't associated with any user-entered data (though it may have initial values).
Receive data from a submit request and bind it to the form.
Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form.
Clean and validate the data.
Cleaning the data performs sanitization of the input fields, such as removing invalid characters that might be used to send malicious content to the server, and converts them into consistent Python types.
Validation checks that the values are appropriate for the field (for example, that they are in the right date range, aren't too short or too long, etc.)
If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.
If all data is valid, perform required actions (such as save the data, send an email, return the result of a search, upload a file, and so on).
Once all actions are complete, redirect the user to another page.
Django provides a number of tools and approaches to help you with the tasks detailed above. The most fundamental is the Form class, which simplifies both generation of form HTML and data cleaning/validation. In the next section, we describe how forms work using the practical example of a page to allow librarians to renew books.

# View
As discussed in the Django form handling process above, the view has to render the default form when it is first called and then either re-render it with error messages if the data is invalid, or process the data and redirect to a new page if the data is valid. In order to perform these different actions, the view has to be able to know whether it is being called for the first time to render the default form, or a subsequent time to validate data.

For forms that use a POST request to submit information to the server, the most common pattern is for the view to test against the POST request type (if request.method == 'POST':) to identify form validation requests and GET (using an else condition) to identify the initial form creation request. If you want to submit your data using a GET request, then a typical approach for identifying whether this is the first or subsequent view invocation is to read the form data (e.g. to read a hidden value in the form).

The book renewal process will be writing to our database, so, by convention, we use the POST request approach. The code fragment below shows the (very standard) pattern for this sort of function view.

