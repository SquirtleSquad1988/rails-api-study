# Rails as an API Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

Please note:

-   Many of the readings will mention the "view" layer. We won't be covering the
    view layer in this program.
-   We'll use our [Rails API Template](https://github.com/ga-wdi-boston/rails-api-template)
    repository as the basis for our rails applications.
    This template excludes the "view" layer.

## Required Readings

-   Better Explained
    -   [Starting Ruby on Rails: What I Wish I Knew](http://betterexplained.com/articles/starting-ruby-on-rails-what-i-wish-i-knew/)
        (sections 3 and 4)
    -   [Intermediate Rails: Understanding Models, Views and Controllers](http://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/)
        (up to and including "Quick Controllers")
-   Ruby on Rails Guides
    -   [Rails Routing from the Outside](http://guides.rubyonrails.org/routing.html)
        (up to and including chapter 2.6)
    -   [Action Controller Overview](http://guides.rubyonrails.org/action_controller_overview.html)
        (up to and including chapter 4.5)
    -   [The Rails Command Line](http://guides.rubyonrails.org/command_line.html)
        (up to and including chapter 1.4)

## Additional Resources

-   [Getting Started with Rails — Ruby on Rails Guides](http://guides.rubyonrails.org/getting_started.html)

## Define Model Responsiblities

In your own words, define what the responsibilities of the model layer are in
Rails.

```md
Models are Ruby classes that act as a middle-man between the controller and database. Models receive information from the controller in the form of controller actions and then talk to the database in order to retrieve or modify from it and ultimately pass it back to the controller.
```

## Define Controller Responsiblities

In your own words, define what the responsibilities of the controller layer are
in Rails.

```md
The controller layer of Rails receives information from the router that tell it which action to retrieve or save information from the model. The controller in addition uses the data from the model and sends it to the view to create HTML output. The controller is thus a middle-man for the view and the model as well as also receiving information from the router.
```

## Define Router Responsiblities

In your own words, define what the router does in Rails.

```md
A router in Rails receives a request from the server in the form of URLs and a verb and tries to match the request to a controller action. The following controller action that is executed is dependent on the information it receives from the router in the form a specific path and HTTP verb.
```

## The Request-Response Cycle in Rails

Starting with a client making a GET request to a particular URL, describe how
the parts of Rails interact to produce and send a response.

```md
When a client makes a GET request to a particular URL the web server will receive the data and pass the URL and request type (verb) to the router. The router then interprets the data and matches it to a controller action in the controller. The controller action will send a request to the model which tells it what to do to the database whether it be delete, modify or create new entry. The model sends this information back to the controller when sends the information the view which ultimately is what is displayed on the client's browser. The data that is transfered to the view by the controller includes HTML, CSS, XML, JavaScript, and JSON. Finally the response is sent to the server and finally back to the user in the form of a HTTP response.
```
