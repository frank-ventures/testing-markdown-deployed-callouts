# testing-markdown-deployed-callouts

Let's see what different quote/callout blocks look like when deployed on Github pages.

## Introduction: The quote block

> **💭 Quotes!**
>
> This is a quote block.
>
> You may have seen them before. You can use them to, well, quote text.
>
> They get shown in a kinda grey font colour I don't really like. But not with some CSS applied!

In markdown you create quotes using a `>` character at the start of multiple lines.

### Edit their style

It's very easy to achieve this look!

To edit the styling of **every** blockquote on a deployed GitHub page, you need an `assets/css/style.css` file. Target the `blockquote` HTML element and your styles will apply. Job done 🎉.

```css
blockquote {
  color: black;
  padding: 0.25em 1em;
  border-left: solid 0.25rem rgba(201, 201, 201, 1);
}
```

If you make the first line of the quote **bold** by using `**asterisks**`in your markdown, this translates to a `<strong>` element, so just target that in your CSS if you want to customise it:

```css
blockquote strong {
  font-family: ;
  font-size: 1.25rem;
}
```

### Custom `blockquotes`

I guess if you want custom blockquotes on your deployed GitHub page (as in, ones which have different styling dependent on their content like the examples below) then you'd have to use HTML in your README file and use the `blockquote` element with CSS classes, combined with the stylesheet explained above.

Read on!

## Notice blocks! - Great on GitHub, pants when deployed

Woah, look at these guys!

Well actually, look at them in a GitHub repo because that's where you'll see their unique styling. On a deployed page they will not show up. Boo 👎

> [!NOTE]
> This is a note block. What does it look like when deployed? Well, if you're looking at it, it looks like this...

> [!TIP]
>
> **We also have tips!**
>
> Tips are cool. Tips are like, "Hey here's a secret you didn't know!"
>
> Tips!

> [!WARNING]
>
> These originated from a band called Green Day.

> [!CAUTION]
>
> Caution, this caution is different to a Warning. Why? Who knows

> [!IMPORTANT]
>
> Important stuff is very important!

## Just using regular HTML

Annoyingly then, unless you install some extra markdown extensions, perhaps the best _(and only)_ way to get a set of styled `blockquote`s when you're using deployed Github pages is to use the `<blockquote>` HTML element with some good old CSS classes.

We can make our own Note boxes

<blockquote class="note">
<strong>Note!</strong>

Take note of this, dear user!

</blockquote>

Our own tip boxes:

<blockquote class="tip">

**Tip!**

Some kinda really very helpful tip would go here.

And some extra bonus stuff.

You can still type regular text, no need for `<p>` tags

</blockquote>

and so on and so on.

<details markdown="1"> <summary>The blockquote CSS:</summary>

```css
.note {
  background-color: rgba(102, 255, 0, 0.2);
  color: black;
  padding: 0.25em 1em;
  border-left: solid 0.25rem rgba(0, 136, 18, 1);

  strong {
    color: darkgreen;
  }
}

.tip {
  background-color: rgba(0, 153, 255, 0.2);
  color: black;
  padding: 0.25em 1em;
  border-left: solid 0.25rem rgba(0, 47, 255, 1);

  strong {
    color: darkblue;
  }
}
```

</details>

Perhaps you could have some kind of **template** file, where you store these bits of HTML, and then your users can just copy/paste those in when needed.

Custom CSS can also be used really well to point out details tags:

<details markdown="1"> <summary>Holy moses I am a clickable details tag!:</summary>

and I am some secret information, woah!

But seriously, this is another place where some simple CSS can really come in handy if you rely on deployed README GitHub pages.

</details>

Good stuff eh?

<details markdown="1"> <summary>The details CSS:</summary>

```css
details {
  border-left: 2px solid rgba(199, 162, 41, 1);
  padding-left: 1rem;
}

details[open] {
  background-color: rgb(0, 0, 0, 0.1);
}
```

</details>

# Real World Example

## Workshop

> **💭 Key Tip: What Google Say**
>
> A notebook in NotebookLM is a collection of sources for a specific project.
>
> Each notebook is independent. NotebookLM can’t access information across multiple notebooks at the same time.

### To Start

1. ⛳️ Go to [notebooklm.google.com](https://notebooklm.google.com/).
2. ⛳️ On that page, click "Create new notebook".

### Creating your Notebook

The main steps to creating a good Notebook are:

1. ⛳️ Upload a source in the popup window _(you may get taken to a 'new' page after uploading just one; that's OK!)_

2. ⛳️ Continue to add sources using the `Sources` pane on the left.

From here, you can ask questions of your Notebook to test how well it functions. Add more `Sources` if you need to and explore the options!

<blockquote class="tip">

**💭 Key Tip: Source Types**

NotebookLM supports these source types:

- Audio files

- Copy and pasted text

- Google Docs

- Google Slides

- Text, Markdown and PDF files

- Web URLs

- YouTube URLs of public videos
</blockquote>
