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

## Android: Difference between Parcelable and Serializable?

In Android we know that we cannot just pass objects to activities. The objects must be either implements Serializable or Parcelable interface to do this.

**Serializable**

Serializable is a standard Java interface. You can just implement Serializable interface and add override methods.The problem with this approach is that reflection is used and it is a slow process. This method create a lot of temporary objects and cause quite a bit of garbage collection. Serializable interface is easier to implement.

**Parcelable**

Parcelable process is much faster than serializable. One of the reasons for this is that we are being explicit about the serialization process instead of using reflection to infer it. It also stands to reason that the code has been heavily optimized for this purpose.

Source- [link](https://stackoverflow.com/a/23647471/1092989)
