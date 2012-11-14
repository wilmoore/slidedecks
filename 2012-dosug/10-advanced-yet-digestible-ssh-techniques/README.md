10 advanced, yet digestible SSH techniques
=================================================


Introduction + About Me
-----------------------------------------

Hey everyone...my name is Wil Moore III

I work for Net-Results...a marketing automation company in Golden.

As a Full-Stack web developer, on a daily basis, I work in multiple
programming languages such as Ruby, JavaScript on the server and 
browser, and PHP, as well as devops and user interface work.

I should start off by sharing with you, why I like this topic. Why SSH?

See, early on in my career, SSH seemed like a black box. I knew the
basics, but all you could do with SSH hadn't yet clicked.

Fast forward to when I started doing more continuous integration as part
of a continuous delivery strategy...that's when it all came together.

So tonight, I'll share with you a few semi-advanced techniques that
won't seem very-advanced once we get em' to click for you.

Now, if you're already an SSH wizard...this'll be more of a refresher.

That being said, how many of you (show of hands) are already familiar
with SSH?

OK, so, this talk is 10 SSH techniques; however, we are going to do a
quick refresher first.


Key Generation Style
-----------------------------------------

You are all likely familiar with generating keys; however, I'd like to
share with you the key generation style that I use. I encourage you to
come up with your own; but this is mine.

We generate `rsa` keys with a comment consisting of a user, an application,
and an environment. In this example, we create a key for a "deploy"
user in an application called "uworkremote" and the environment is CI
(continuous integration).

As you can see, this style scales well in multi-environment setups.

I'm sure you've seen $HOME/.ssh/id_rsa.

This is a terrible default. It alludes to only ever using a single key pair.

This isn't realistic; you don't want to use the same key everywhere.
Now, keep it reasonable of course, but one key for everything is not a good
idea security-wise.

In other words, when you build your startup app on Amazon EC2 don't go sharing
those EC2 keys with the nodes back at your 9-5.

