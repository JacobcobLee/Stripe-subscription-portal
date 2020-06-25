# Subscriptions with fixed price

Create a subscription for an online service with fixed-price options, and work with Stripe Elements to host a payment form on your servers.
This sample shows how to create a customer, set up a card for recurring use, and subscribe them to a subscription plan with
[Stripe Billing](https://stripe.com/billing).

////////////////////////////////////////////////////////////////////////////////
//                       before you run do the following:                     //
////////////////////////////////////////////////////////////////////////////////
- make sure you have your own env file
- make sure to have npm install in main folder and server/node!

### Features:

- 💳Securely collect card details
- 🔒Save the payment method details to a customer
- 🚫Handle payment failures
- 💰Subscribe the customer to a subscription plan
- ➕Upgrade and downgrade on prices

## How to run locally

This sample includes [5 server implementations](server/) in our most popular languages. Follow the steps below to run one of the servers locally.

**1. Clone and configure the sample**

The Stripe CLI is the fastest way to clone and configure a sample to run locally.

**Using the Stripe CLI**

If you haven't already installed the CLI, follow the [installation steps](https://github.com/stripe/stripe-cli#installation) in the project README. The CLI is useful for cloning samples and locally testing webhooks and Stripe integrations.

In your terminal shell, run the Stripe CLI command to clone the sample:

```
stripe samples create subscription-use-cases
```

The CLI will walk you through picking your integration type, server and client languages, and configuring your `.env` config file with your Stripe API keys.

**Installing and cloning manually**

If you do not want to use the Stripe CLI, you can manually clone and configure the sample:

```
git clone git@github.com:stripe-samples/subscription-use-cases.git
```

Copy the `.env.example` file into a file named `.env` in the folder of the server you want to use. For example:

```
cp .env.example server/node/.env
```

You will need a Stripe account in order to run the demo. Once you set up your account, go to the Stripe [developer dashboard](https://stripe.com/docs/development#api-keys) to find your API keys.

```
STRIPE_PUBLISHABLE_KEY=<replace-with-your-publishable-key>
STRIPE_SECRET_KEY=<replace-with-your-secret-key>
```

`STATIC_DIR` tells the server where the client files are located and does not need to be modified unless you move the server files.

**2. Create Products and Plans on Stripe**

This sample requires a [Price](https://stripe.com/docs/api/prices) ID to create the subscription. Products and Plans are objects on Stripe that you use to model a subscription.

You can create Products and Prices [in the Dashboard](https://dashboard.stripe.com/products) or with the [API](https://stripe.com/docs/api/prices/create). Create a Price to run this sample and add it to your `.env`.

**3. Follow the server instructions on how to run:**

Pick the server language you want and follow the instructions in the server folder README on how to run.

```
cd server/node # there's a README in this folder with instructions
npm install
npm start
```
