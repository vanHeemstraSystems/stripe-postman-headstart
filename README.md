stripe-postman-headstart
# Stripe Postman - Headstart

Based on "Getting Started with Stripe Postman" at https://www.youtube.com/watch?v=oviFGXrwYIQ

Postman collection at https://www.postman.com/stripedev/workspace/stripe-developers/overview

## 100 - Introduction

Learn how to use the Stripe public Postman collection to make test API calls to Stripe. Our new Postman collection includes templates all our API resources and makes it easy to explore Stripe's APIs and scaffold integrations without writing code.

## 200 - Getting your API secret key

Make sure you have registered with [Stripe](stripe.com).

Also, make sure you are in **Test Mode**, so not in Production Mode. This is indicated on the dashboard, where you will go next. You do not want to make Postman calls with your production key.

Go to the following URL to collect the API secret key: https://dashboard.stripe.com/test/dashboard

It will look something like:

```
sk_test_............................................................................
```

## 300 - The Stripe Dev profile and workspace

Make sure you have an account with [Postman](https://www.postman.com/downloads/) and are signed in.

Open [Postman](https://www.postman.com) and from the search bar look for ***StripeDev***. 

![image](https://user-images.githubusercontent.com/12828104/148941214-df1eb29e-3dab-47cc-a4ae-dda55a4c27a6.png)

Postman StripeDev collection

This should open [StripeDev](https://www.postman.com/stripedev) (only when you are signed into Postman):

![image](https://user-images.githubusercontent.com/12828104/148942595-312216d5-7a1f-474c-82ae-0a1a3327ee8c.png)

StripeDev Workspace - Stripe API

Click on **Stripe API**, the one without the date. It will open in Postman.

## 400 - Forking the Stripe API collection

![image](https://user-images.githubusercontent.com/12828104/148943667-575e7086-a0c0-4e2d-a287-a44f28cf3318.png)

Stripe Developers - Stripe API

This is a postman collection covering the Stripe API. See https://stripe.com/docs/api for more details.

Create a fork, by opening the dropdown menu from Stripe API as shown below:

![image](https://user-images.githubusercontent.com/12828104/148944568-f62b2580-0adb-44bb-b77f-84438c38fc05.png)

Stripe Developers - Stripe API - Create a fork

Forking creates a copy of the collection in your account. You can use its requests or suggest changes without affecting the original.

Complete the following fields as follows:

- Fork label: **My StripeDev Fork** (or any other label you want to give it instead)
- Location: **My Workspace** (or any other workspce you want it to be located)

![image](https://user-images.githubusercontent.com/12828104/148945524-aa95edac-8d90-43e7-89ba-11157441a9e2.png)

Stripe API - Fork collection

You can check ```Watch original collection```, if you so please. It is not mandatory.

Next, click the **Fork Collection** button.

You will be prompted as follows:

![image](https://user-images.githubusercontent.com/12828104/148946669-1c518891-1dcd-4cb7-9b7c-0fd7c3ebea7c.png)

Make your profile public.

Here you can decide to agree, then click the **Make Profile Public** button.

![image](https://user-images.githubusercontent.com/12828104/148947190-42fca280-6175-492c-b937-4dc4c8e4bdea.png)

After some time, the Stripe API (here: My StripeDev Fork) will appear in your Postman Workspace (here: My Workspace).

![image](https://user-images.githubusercontent.com/12828104/148951139-041d4e01-3989-4d80-b857-eaab994ecd2b.png)

## 500 - Forking the Stripe Environment template

Instead of forking the Stripe Environment, we create a new Environment as shown below:

![image](https://user-images.githubusercontent.com/12828104/148951139-041d4e01-3989-4d80-b857-eaab994ecd2b.png)

Stripe - Create Environment

![image](https://user-images.githubusercontent.com/12828104/148952040-83a07fca-1564-4b18-b3e1-99675683ee49.png)

Rename Stripe Environment to "Stripe Environment Template"

Next, we add one variable labeled **secret_key**

![image](https://user-images.githubusercontent.com/12828104/148952922-832a7cb9-1ff1-471a-8dcf-1227af70dde3.png)

Stripe Environment Template - secret_key

Enter in the **Current Value** field, the value of the **Secret Key** as captured from your Stripe's Dashboard earlier.

![image](https://user-images.githubusercontent.com/12828104/148953703-ab507ae1-2443-45a6-95bc-9260698fde44.png)

Stripe Environment Template - Current Value: Secret Key





== WE ARE HERE ==

## 600 - Setting up authentication 

## 700 - Navigating the collection

## 800 - Testing the Stripe Checkout API with Postman

## 900 - Testing the Customers API with Postman

## 1000 - Using variables

## 1100 - Outro
