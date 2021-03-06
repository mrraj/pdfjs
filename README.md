[![Build Status](https://travis-ci.org/mohanraj-ramanujam/pdfjs.svg?branch=master)](https://travis-ci.org/mohanraj-ramanujam/pdfjs)
[![Gem Version](https://badge.fury.io/rb/pdfjs.svg)](http://badge.fury.io/rb/pdfjs)

### PDFJS Information

PDFJS is a RAILS ENGINE plugin for integrating the PDFJS into the RAILS applications.

* Is a RAILS ENGINE;
* Is composing of PDFJS images, javascripts and stylesheets;
* Is contains PDFJS HTML layout;

## Installation

Add this line to your application's Gemfile (Rails):

    gem 'pdfjs'
    
And then execute:

    $ bundle

* Create a separate controller inherited from Pdfjs::PdfjsController

  ```ruby
  class PDFController < PdfjsController
  end
  ```

* Define your action. EX: show.

  ```ruby
  class PDFController < PdfjsController
    def show
      @pdfjs_file = 'http://yoursite.com/pdfjs.pdf'
    end
  end
  ```

* Create the show template and set the PDF file path

  ```html
  <%= content_for :pdfjs do %>
    <%= javascript_tag do %>
      window.DEFAULT_URL = '<%= @pdfjs_file.html_safe %>';
    <% end %>
  <% end %>
  ```

### Example applications

* https://github.com/mohanraj-ramanujam/pdfjs_integration

### Contribution

Feel free to give pull request if you interested to fix some issues/features. Thanks.
