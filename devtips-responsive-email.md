# Dev Tips Responsive Email Notes

---

### Things to keep in mind

* Don't use tables to create the layout, they are considered outdated.

* All styles are done inline.

* Never style the body element.

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

</html>

```

---

### Step 3

Now we are going to create the ***pre-header***. This is the first few words that people see when they open up your email and make the decision on wether they want to continue reading or trash it. Pre-header is nested in the email-background div but before the email-container div.

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

</html>

```

---

### Step 4
