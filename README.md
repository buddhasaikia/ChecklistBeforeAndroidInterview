# Interview Cheat Sheet
Android interview check list just before interview. Answers have been curated from internet (mainly stackoverflow, android developer guide)

## Different types of intent

**Implicit intent**
Implicit Intents do not directly specify the Android components which should be called , it only specifies action to be performed.
e.g. Intent intent = new Intent(ACTION_VIEW,Uri.parse("http://www.google.com");

**Explicit intent**
Explicit intents are used in the application itself wherein one activity can switch to other activty.
Intent intent = new Intent(this,TargetActivity.class);

Source- [link](https://stackoverflow.com/a/13329731/1092989)
