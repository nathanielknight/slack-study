# Surfaces

A **surface** is anywhere an app can "express" itself via communication or UI.

Apps are intended to be ubiquitous, using whatever surface is convenient for
the task at hand, not cram everything into a single point of interaction.


## Home Tab

An app's home tab is a persistent view accessible via Slack's App menu.

It's unique for each user of the app. It's within the larger "App Home" which
also has an about tab and a record of the messages between the user and the
app.

The Home tab's content can be updated anytime, and will persist until a new
update. An app must have at least one *scope* to use its home tab.

The main ways to implement the home and messages tab are by subscribing to the
`app_home_opened` and `message.im` events (detect when a user opens the app home
or messages your app and reply appropriately).


## Modals

Modals are intrusive UI elements composed of 1-3 block-kit views in a **stack**
that can **only** appear in response to user interaction. They hold focus until
submitted or dismissed. 

Modals can be updated while they're open, including pushing new views. Views
are popped when they're submitted or cancelled.


## Messages

Just like messages from other users, but from an App or bot. Once the necessary
permissions have been granted, an app can send a message unbidden, forming a
jumping-off point for further interaction.

As one might expect from a messaging app, the messages API is complex enough to
warrant its own section.
