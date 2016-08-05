---
layout: page
title: Users
---

# Users

A small, yet significant, part of Anchor is the ability to allow for multiple
users. A user is simply someone who can access the Administration interface, to
do all the functions that any other user (including yourself) can do.
Essentially, a *user* is an *administrator* of the blog, for this purpose, the
docs will refer to a user as an admin.

## The Users screen

![Anchor’s users screen](/images/users-list.png)
This screen will show you all of the admins currently registered, indeterminate
of whether or not they are active or inactive (more on that later).

## Creating/editing a user

To create a user, simply click the green "Create a new user" button. Displayed
will be a simple form asking for details about the new user.

![Anchor’s new user screen](/images/users-new.png)

Each of the fields are explained below.

## Real Name

This field is the Display Name of the admin. A username or a pseudonym can be
used as Anchor doesn't force a name validation on this field. Any character is
available for use in this field.

## Biography

This field isn't mandatory, however it is useful for displaying information
about an admin, as blogs often do. Any character is available for use in this
field.

## Status

Use this to determine whether an Admin has become inactive, or whether they are
to become active. This field is used specifically when logging in to determine
if the user is allowed to access the Admin area.

## Username

This field is a unique identifier for the admin account, this it is not allowed
to be the same as other usernames - Anchor will notify you of this. This is also
what the user will log in with. Any character is available for use in this
field, however it's advised to stick to alphanumeric with no spaces.

## Password

This field is how users are authenticated to prevent security holes within
Anchor. This is also what the user will log in with.

## Email

This field is used as a fallback should you forget your password. If you have
forgotten your password, an email will be sent to this account. It is important
that you ensure this is correct.
