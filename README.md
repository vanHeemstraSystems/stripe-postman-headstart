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

Enter in the **Current Value** field, the value of the **Secret Key for Test** as captured from your Stripe's Dashboard earlier.

![image](https://user-images.githubusercontent.com/12828104/148953703-ab507ae1-2443-45a6-95bc-9260698fde44.png)

Stripe Environment Template - Current Value: Secret Key

And do not forget to click the **Save** button to save the Stripe Environment Template with the Current Value set.

## 600 - Setting up authentication 

Go back to the Collections in My Workspace and reselect Stripe API. Make sure you select **Stripe Environment Template** as the Environment so the secret_key variable is accessible.

![image](https://user-images.githubusercontent.com/12828104/148955792-09d316b1-473c-4ca4-affc-6039136073ea.png)

Select Stripe Environment Template with the Stripe API Collection.

Replace the value of **Token** by ```{{secret_key}}```:

![image](https://user-images.githubusercontent.com/12828104/148960749-3302b4ed-a57a-4e4c-b958-7f1be16934ed.png)

Secret Key as Token

Make sure to click the **Save** button afterwards. 

That's it for setting up the authentication.

## 700 - Navigating the collection

The Stripe API Postman Collection has a folder for every API resource Stripe has (e.g. Accounts, Persons, etc).

If you look in any of the folders you will se that it has multiple requests.

For example:

**Checkout**:

- List all Checkout Sessions
- Create a Session
- Retrieve a Session
- Expire a Session
- Retrieve a Session's line items

And all the requests represent the actions you can take against this API.

So, in the case of ```Checkout```, which we will be using in a moment, you can retrieve for eaxmple the line items (which are the products that you are selling).

For more information on Checkouts, checkout (pun intended) the video on [Stripe Checkout](https://www.youtube.com/watch?v=UjcSWxPNo18) on Stripe's YouTube Channel.

So, let's create a Checkout Session.

In order to do so, we click on the "***Create a Session***" request, we navigate to the ```body```:

![image](https://user-images.githubusercontent.com/12828104/148966318-6dfaf79e-eae9-4e8b-a107-78d530d67eb8.png)

Create a Session: body

And then all we have to do is fill out the type of request we are building.

There are many keys, but the ones you ***must*** use are ```cancel_url``` and ```success_url``` no matter waht you are doing. So they are checked by default.

![image](https://user-images.githubusercontent.com/12828104/148967520-065702ed-fae9-4f5e-ab5e-157b93daf1d7.png)

Create a Session - mandatory keys

Moving on to the next section!

## 800 - Testing the Stripe Checkout API with Postman

Enter the below values in the form for Create a Session:

| Key | Value |
| --- | --- |
| cancel_url | https://example.com/cancel |
| success_url | https://example.com/success |
| line_items[0][price_data][currency] | usd |
| line_items[0][price_data][product_data][name] | T-shirt |
| line_items[0][price_data][unit_amount] | 2000 |
| line_items[0][quantity] | 1 |
| mode | payment |
| payment_method_types[0] | card |

**Note**: unit amount is in cents, hence why 2000 is 20,00 USD

Now click the **Save** button, followed by **Send**.

As a response we (may) get an error ***400 Bad Request***:

```
{
    "error": {
        "message": "In order to use Checkout, you must set an account or business name at https://dashboard.stripe.com/account.",
        "type": "invalid_request_error"
    }
}
```

Set the ***Account name*** as indicated in above error message at https://dashboard.stripe.com/account :

![image](https://user-images.githubusercontent.com/12828104/148975652-34e0510c-ae4d-4030-b813-a23aff561b33.png)

Stripe Account Name (can be anything, here ```MyCompany```)

Save the setting of the ***Account Name*** in Stripe, then push the "***Send***" button again in Postman.

This time we should get a successful response **200 OK**:

```
{
    "id": "cs_test_a1iIWMWmpKMmj0H8VU9shhzQaty53jyZMS0VSltGwgwQ0clxvPMTH7Vxwv",
    "object": "checkout.session",
    "after_expiration": null,
    "allow_promotion_codes": null,
    "amount_subtotal": 2000,
    "amount_total": 2000,
    "automatic_tax": {
        "enabled": false,
        "status": null
    },
    "billing_address_collection": null,
    "cancel_url": "https://example.com/cancel",
    "client_reference_id": null,
    "consent": null,
    "consent_collection": null,
    "currency": "usd",
    "customer": null,
    "customer_details": null,
    "customer_email": null,
    "expires_at": 1642002844,
    "livemode": false,
    "locale": null,
    "metadata": {},
    "mode": "payment",
    "payment_intent": "pi_3KGmfgAoGYTOOZ9a1HbwOqhF",
    "payment_method_options": {},
    "payment_method_types": [
        "card"
    ],
    "payment_status": "unpaid",
    "phone_number_collection": {
        "enabled": false
    },
    "recovered_from": null,
    "setup_intent": null,
    "shipping": null,
    "shipping_address_collection": null,
    "shipping_options": [],
    "shipping_rate": null,
    "status": "open",
    "submit_type": null,
    "subscription": null,
    "success_url": "https://example.com/success",
    "total_details": {
        "amount_discount": 0,
        "amount_shipping": 0,
        "amount_tax": 0
    },
    "url": "https://checkout.stripe.com/pay/cs_test_a1iIWMWmpKMmj0H8VU9shhzQaty53jyZMS0VSltGwgwQ0clxvPMTH7Vxwv#fidkdWxOYHwnPyd1blpxYHZxWjA0Tj1hQ0xEakJcUUpKXzxkRGBSbFZdfDdqPENJQG58dk1sUWddfUs2SE9qQ2FHMDZiXD1OS2pBYV9%2Fc0RHX3JEYWR1ZHdfTExsf3BNb1RIV3B1aHJBb0pKNTUwf2lMdVFwYCcpJ2N3amhWYHdzYHcnP3F3cGApJ2lkfGpwcVF8dWAnPyd2bGtiaWBabHFgaCcpJ2BrZGdpYFVpZGZgbWppYWB3dic%2FcXdwYHgl"
}
```

Great!

When following the url as given in the response, https://checkout.stripe.com/pay/cs_test_a1iIWMWmpKMmj0H8VU9shhzQaty53jyZMS0VSltGwgwQ0clxvPMTH7Vxwv#fidkdWxOYHwnPyd1blpxYHZxWjA0Tj1hQ0xEakJcUUpKXzxkRGBSbFZdfDdqPENJQG58dk1sUWddfUs2SE9qQ2FHMDZiXD1OS2pBYV9%2Fc0RHX3JEYWR1ZHdfTExsf3BNb1RIV3B1aHJBb0pKNTUwf2lMdVFwYCcpJ2N3amhWYHdzYHcnP3F3cGApJ2lkfGpwcVF8dWAnPyd2bGtiaWBabHFgaCcpJ2BrZGdpYFVpZGZgbWppYWB3dic%2FcXdwYHgl

we will see the form in Stripe, showing our checkout information:

![image](https://user-images.githubusercontent.com/12828104/148977182-8cdebdcb-c298-42e4-b006-1db0de8f0db4.png)

Stripe Checkout Information






== WE ARE HERE ==

## 900 - Testing the Customers API with Postman

## 1000 - Using variables

## 1100 - Outro
