This project includes a simple application that integrates with the Google Apps Marketplace
using OpenID and the Google Data APIs.  It is written in ruby using the Sinatra web framework.

Required gems:
- sinatra
- ruby-openid
- ruby-openid-apps-discovery
- rack-openid
- oauth

The manifest for the application is located in views/manifest.erb.  A complete manifest
can be generated by running the application.

  ruby hello.rb
  curl http://<your_host>/manifest.xml

This manifest can then be used when creating the application in the marketplace.
Instructions for creating a listing can be found at:

  http://code.google.com/googleapps/marketplace/listing.html
  
Once the application has been created in the marketplace, you'll need the generated
OAuth key & secret to run the application.

To run:

  CONSUMER_KEY=<your_key> CONSUMER_SECRET=<your_secret> ruby hello.rb
  
Where <your_key> and <your_secret> are the OAuth key & secret your application
uses to authenticate to Google.

