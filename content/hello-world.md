+++
title = "Hello World"
description = "A quick overview on how to say hello to the world"
date = 2020-08-01
updated = 2020-08-02

[extra]
hidden = false

[taxonomies]
categories = ["misc"]
tags = ["random"]
+++

Hello world! This is an initial article used to test several formatting items from Markdown and displaying how they look like after the page is actually rendered by the theme.

<!-- more -->

And this is the rest of the content. Here in the rest of the content I test a lot of text formatting functions to I can see how it will be rendered. What I want to as well is to show footnotes. So let's say we are using a footnote{{ citation(id=1) }}. So I keep writing, and then I refer another citation{{ citation(id=2) }}. Finally, I still keep going on and refer a third one{{citation(id=3)}}.

First of all, we start with a list. This is a list:

* One item
* Another item
* Yet another item
* Oh look how fast I can type items

Then we move to a numbered list:

1. Start with one item
2. Then move to the next
3. And boom, you have a list.
4. Look how beautiful it is.

Then we want a little bit of code. Let's try some Ruby.

```ruby
require socket

server = TCPServer.new(4000)
client = server.accept
data = client.read
client.write data
client.flush
client.close
server.close
```

Then some HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Test</title>
</head>
<body>
    <h1>test</h1>
</body>
</html>
```

Ok, really beautiful. Now let's try a quoted passage:

> After the time spent in creating the theme, now there was a need to actually create some sample content to showcase it. Without any quotes to add here, I just added one I created on my own, on demand.

Now I also want to use some `formatted` words inside the text. Beautiful. Now let's try go get an image into the page.

{{ image(path="/sample-image.jpg", alt="This is a sample inserted
from a resized image") }}

Now it is here.

{% footnote(id=1) %}
For all sections except the top-level index, you also need to add an `_index.md`.
{% end %}
{% footnote(id=2) %}
With the exception of any `_index.md` files.
{% end %}
{% footnote(id=3) %}
I had problems with the built-in pagination functionality. It seems like it either doesn't work right or I don't understand it and the docs are too sparse. The server works pretty well for content serving, but every once in a while I managed to crash it with some syntax errors. The system that refreshes the browser page when the server rebuilds content also seems to mess up every once in a while, but restarting the server fixes it.
{% end %}