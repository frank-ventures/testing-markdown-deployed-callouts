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

<strong>👀 Note!</strong>

Take note of this, dear user! The "Note" text above uses a 'strong' tag.

Some kinda really very helpful note would go here.

You can still type regular text, no need for 'p' tags! Just beware of how it will render.

</blockquote>

Our own tip boxes, which have CSS classes:

<blockquote markdown="1" class="tip">

**💭 Tip!**

This absolute top tip reminds us that we need to include the attribute `markdown="1"` inside of our HTML tags if we want the included markdown to be formatted correctly.

</blockquote>

<blockquote markdown="1" class="warning">

**⚠️ Warning**

Some kinda thing you should be warned of.

</blockquote>

<blockquote markdown="1" class="caution">

**❗ Caution**

Some kinda thing you should be cautious about.

</blockquote>

<blockquote markdown="1" class="important">

**👀 Important**

Some kinda thing which is of utmost importance.

</blockquote>

<details markdown="1"> <summary>The blockquote CSS:</summary>

```css
blockquote {
  color: black;
  padding: 0.25em 1em;
  border-left: solid 0.25rem rgba(201, 201, 201, 1);
}

.note {
  --dark-colour: #238636;
  --light-colour: #68bf79ff;
  padding: 0.25em 1em;
  border-top: 2px solid var(--light-colour);
  border-bottom: 2px solid var(--light-colour);
  border-right: 2px solid var(--light-colour);
  border-left: solid 0.25rem var(--dark-colour);
}

.tip {
  --dark-colour: #1f6feb;
  --light-colour: #46a3f9ff;
  padding: 0.25em 1em;
  border-top: 2px solid var(--light-colour);
  border-bottom: 2px solid var(--light-colour);
  border-right: 2px solid var(--light-colour);
  border-left: solid 0.25rem var(--dark-colour);
}

.warning {
  --dark-colour: #9e6a03;
  --light-colour: #f9d019ff;
  padding: 0.25em 1em;
  border-top: 2px solid var(--light-colour);
  border-bottom: 2px solid var(--light-colour);
  border-right: 2px solid var(--light-colour);
  border-left: solid 0.25rem var(--dark-colour);
}

.caution {
  --dark-colour: #da3633;
  --light-colour: #ff7984ff;
  padding: 0.25em 1em;
  border-top: 2px solid var(--light-colour);
  border-bottom: 2px solid var(--light-colour);
  border-right: 2px solid var(--light-colour);
  border-left: solid 0.25rem var(--dark-colour);
}

.important {
  --dark-colour: #8957e5;
  --light-colour: #c062ffff;
  padding: 0.25em 1em;
  border-top: 2px solid var(--light-colour);
  border-bottom: 2px solid var(--light-colour);
  border-right: 2px solid var(--light-colour);
  border-left: solid 0.25rem var(--dark-colour);
}

.note > p:first-child,
.tip > p:first-child,
.warning > p:first-child,
.caution > p:first-child,
.important > p:first-child {
  color: var(--dark-colour);
  font-size: 1.25rem;
}

blockquote strong {
  font-size: 1.25rem;
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
>
> _this tip box was made with regular ">" markdown characters_

### To Start

1. ⛳️ Go to [notebooklm.google.com](https://notebooklm.google.com/).
2. ⛳️ On that page, click "Create new notebook".

### Creating your Notebook

The main steps to creating a good Notebook are:

1. ⛳️ Upload a source in the popup window _(you may get taken to a 'new' page after uploading just one; that's OK!)_

2. ⛳️ Continue to add sources using the `Sources` pane on the left.

From here, you can ask questions of your Notebook to test how well it functions. Add more `Sources` if you need to and explore the options!

<blockquote markdown="1" class="tip">

**💭 Key Tip: Source Types**

NotebookLM supports these source types:

- Audio files

- Copy and pasted text

- Google Docs

- Google Slides

- Text, Markdown and PDF files

- Web URLs

- YouTube URLs of public videos

_this tip box was made with the blockquote HTML element_

</blockquote>
