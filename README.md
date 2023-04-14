# Chronosong

Discover the randomness of Spotify in this quick little game.

Connect to Spotify and play a game where you get 5 rounds with random songs and get to guess which year it was released! What's your best score?


***Unfortunately, Spotify does not allow public access for games or quizzes, so feel free to REQUEST ACCESS by sending me your Spotify email and I can add you to the app privately.*** (but here is a free spotify account that has access email: pw: )


You can also recreate the app by downloading the files, creating a developer account with Spotify, adding the app and changing the client ID, website and redirect URIs in the dashboard, as well as in the files here:

const clientId = "dbaf8fe7fce641d98710a68e488edf81";
const redirectUri = "https://chronosong2.pages.dev";

Change script.js lines 20 and 21
to
const clientId = YOUR_CLIENT_ID
const redirectUri = "http://127.0.0.1:5000";

Then create a folder called 'templates' and add index.html in it.
Then create a folder called 'static' and add style.css and script.js in it.
Then edit the index.html file on lines 13 and 21 so that the src to the css and js files are: 'static/script.js" and 'static/style.css'.

Finally, create a main.py file with the following:

"from flask import Flask, render_template
app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')

if __name__ == "__main__":
    app.run()"

Hope you enjoy!


Credits to the Spotify API, Chronophoto.app and @rob_medico for inspiration.
