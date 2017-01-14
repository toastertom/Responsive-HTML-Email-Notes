# Dev Tips Responsive Email Notes

---

### Things To Keep In Mind

* Don't use tables to create the layout, they are considered outdated.

* Mobile First ***Always***.

* All styles are done inline because some email services don't read <style> tags.

* Some email services chop off the <head> so don't put anything there.

* Never style the body element.

* Keep it single column (most people view email via mobile).

* Don't waste time on creating directories to organize the files. The email should be simple, clean and probably will never be used again (Unless you want a template).

* Pro tip: put your <styles> in the <head> then use this tool to make your css inline [CSS Inliner Tool](https://templates.mailchimp.com/resources/inline-css/). Then delete the <head> and <style> tags.

---

### Step 1
Start by creating a regular HTML document.

```

<!DOCTYPE html>
<html>
  <head>
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
