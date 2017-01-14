# Dev Tips Responsive Email Notes

---

### Things To Keep In Mind

* Don't use tables to create the layout, they are considered outdated.

* Mobile First ***Always***.

* All styles are done inline because some email services don't read style tags.

* Some email services chop off the head so don't put anything there.

* Never style the body element.

* Keep it single column (most people view email via mobile).

* Don't waste time on creating directories to organize the files. The email should be simple, clean and probably will never be used again (Unless you want a template).

* Pro tip: put your style tag in the head then use this tool to make your css inline ([CSS Inliner Tool](https://templates.mailchimp.com/resources/inline-css/)). Then delete the head and style tags.

---

### Step 1
Start by creating a regular HTML document and put your styles in the head of the document.

```

<!DOCTYPE html>
<html>
  <head>
    <style>

    </style>
  </head>

  <body>
  </body>
</html>

```

---

### Step 2

We never style the body element so make a div element with the class of "email-background" that we can style for the background. Also create another div element nested inside the email-background div called "email-container".

```

  <body>

  <div class="email-background">

    <div class="email-container">

    </div>

  </div>

  </body>

```

---

### Step 3

Now we are going to create the ***pre-header*** which is the short summary text that follows the subject line when an email is viewed in the inbox. Many mobile, desktop and web email clients provide them to tip you off on what the email contains before you open it. Pre-header is nested in the email-background div but before the email-container div and will also have to be hidden.

```

  <body>

  <div class="email-background">

    <div class="pre-header">
      5 tips for creating a responsive email!
    </div>

    <div class="email-container">

    </div>

  </div>

  </body>

```

---

### Step 4

Do all your regular HTLM designs inside the email-container div. Remember try to make the layout simple and in a single column.

---

### Step 5

Style your document using the style tags in the head.

```
<head>
  <style>

    .email-background {
      background-color: #eee;
    }

  </style>
</head>

```

---

### Step 6

Once you are done styling your document create a second copy and call it "whateveryouwant-inline.html", then go to [CSS Inliner Tool](https://templates.mailchimp.com/resources/inline-css/). Copy and paste all of your code into the tool and let it make all the styles inline for you. Once thats done copy the new code into your "whateveryouwant-inline.html" file.

---

### Step 7

Now that you have all your code inline you will want to go through and delete your DOCTYPE!, html, head, style, and body tags. Gmail removes these anyways but you want to make sure everything still works on your end without them.

```
<!-- This is all that there will be -->

<div class="email-background" style="background-color: #eee">

  <div class="pre-header">
    5 tips for creating a responsive email!
  </div>

  <div class="email-container">

  </div>

</div>


```

---

#END
