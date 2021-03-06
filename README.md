# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

ExecJS supports these runtimes:

therubyracer - Google V8 embedded within Ruby

therubyrhino - Mozilla Rhino embedded within JRuby

Node.js

Apple JavaScriptCore - Included with Mac OS X

Microsoft Windows Script Host (JScript)

Depending on your application's configuration some manual setup may be required:

  1. Ensure you have defined default url options in your environments files. Here
     is an example of default_url_options appropriate for a development environment
     in config/environments/development.rb:

       config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

     In production, :host should be set to the actual host of your application.

     * Required for all applications. *

  2. Ensure you have defined root_url to *something* in your config/routes.rb.
     For example:

       root to: "home#index"

     * Not required for API-only Applications *

  3. Ensure you have flash messages in app/views/layouts/application.html.erb.
     For example:

       <p class="notice"><%= notice %></p>
       <p class="alert"><%= alert %></p>

     * Not required for API-only Applications *

  4. You can copy Devise views (for customization) to your app by running:

       rails g devise:views

     * Not required *

//= require rails-ujs
//= require activestorage
//= require turbolinks
//= require_tree .

<div class="form-group col-md-6">
        <div class="col-md-12">
          <%= p.label :card_expires, "Card Expires", data: { stripe: 'label'} %>
        </div>

        <div class="col-md-3">
          <%= p.select :card_expires_month, options_for_select(Payment.month_options), 
              { include_blank: 'Month' }, "data-stripe" => "exp-month", class: "form-control", 
              required: true %>
        </div>

        <div class="col-md-3">
          <%= p.select :card_expires_year, options_for_select(Payment.year_options.push), 
              { include_blank: 'Year' }, class: "form-control", data: { stripe: "exp-year" }, 
              required: true %>
        </div>
      </div>

* ...
