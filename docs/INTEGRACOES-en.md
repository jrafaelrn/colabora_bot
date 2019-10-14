## Bot integrations
Here are the bot integrations.
> Warning: These settings are optional for the bot's DEBUG mode operations.

### On Twitter

You must get your tokens to use the Twitter API:

1. Create your account normally if you don't have one.
2. Then apply for a developer account [here](https://developer.twitter.com/en/apply/user).

Today the request can take days (and there are reports of people who never received). Be as descriptive as possible about your project and keep an eye out for emails, as Twitter may request additional information. It is also by email that Twitter will notify you that your request has been accepted. If this happens: celebrate (yahoo!) And create an app by clicking [here](https://developer.twitter.com/en/apps). This will give you access to your tokens which are: consumer_key, consumer_secret, access_token and access_token_secret.

Put your tokens in the `.env` file as shown.

### On Mastodon

1. Create an account on the instance of your choice. We chose [Bots in Space](https://botsin.space/about/more), but the procedure should be similar to any other. Make sure that the bot you are configuring will not violate the terms of conduct of the instance of your choice, as the rules may differ!

2. Register your bot in the instance by running the code below:

```python
from mastodon import Mastodon

Mastodon.create_app(
     'colaborabot',
     api_base_url = 'https://botsin.space',
     to_file = 'colaboradonte_clientcred.secret'
)
```

Then run the following code:

```python
from mastodon import Mastodon

mastodon = Mastodon(
    client_id = 'colaboradonte_clientcred.secret',
    api_base_url = 'https://botsin.space'
)
mastodon.log_in(
    'seu_login@servidor.com',
    'senhamuitoboaesupersegura',
    to_file = 'colaboradonte_usercred.secret'
)
```

Be sure to modify the parameters as needed.

3. Retrieve the created keys `pytooter_clientcred.secret` and `pytooter_usercred.secret` insert them into the `.env` file.

* [Original documentation](https://mastodonpy.readthedocs.io/en/stable/#) of the used authentication library.

### Google Sheets

To use Google Sheets, we use the [gspread](https://gspread.readthedocs.io/en/latest/) library along with [Authlib](https://blog.authlib.org/2018/authlib-for-gspread) for authentication.

1. The first step is to get a Google Sheet app access token. Visit the [Google API Console](https://console.developers.google.com/project) and create a project (or select one you have already created).

2. In the left-hand menu, select "Credentials" and click the "Create Credentials" button by choosing "Service Account Key". Choose the json format and save the file to your computer.

3. This file should be inserted into the `credenciais\colaborabot-gAPI.json` folder, as described in the `autenticadores.py` program.
