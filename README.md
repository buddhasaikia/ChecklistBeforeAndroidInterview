# Interview Cheat Sheet
Android interview check list just before interview. Answers have been curated from internet (mainly stackoverflow, android developer guide)

## What is intent? What are different types of intent?

Intents are the standard messaging mechanism in Android that expresses the user’s intention to perform some work. They allow you to interact with other components defined by you or by the Android operating system.

**Implicit intent**
Implicit Intents do not directly specify the Android components which should be called , it only specifies action to be performed.
e.g. `Intent intent = new Intent(ACTION_VIEW,Uri.parse("http://www.google.com");`

**Explicit intent**
Explicit intents are used in the application itself wherein one activity can switch to other activty.
`Intent intent = new Intent(this,TargetActivity.class);`

**Pending intent**
A PendingIntent specifies an action to take in the future. It lets you pass a future Intent to another application and allow that application to execute that Intent as if it had the same permissions as your application.

Source- [link 1](https://stackoverflow.com/a/13329731/1092989), [link 2](https://stackoverflow.com/a/15873786/1092989)
