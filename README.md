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
[Some Text](some-url){ .btn .btn-primary }

### Edit their style

It's very easy to achieve this look!

To edit the styling of **every** blockquote on a deployed GitHub page, you need an `assets/css/style.css` file. Target the `blockquote` HTML element and your styles will apply. Job done 🎉.

```css
blockquote {
  background-color: rgba(255, 174, 0, 0.25);
  color: black;
  padding: 0.25rem;
  border-left: solid 0.25rem rgba(255, 174, 0, 1);
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

## Notice blocks! - Great on GitHub, pants when deployed

Woah, look at these guys!

Well actually, look at them in a GitHub repo because that's where you'll see their unique styling. On a deployed page they will not show up. Boo 👎

> [!NOTE]
> This is a note block. What does it look like when deployed? Well, if you're looking at it, it looks like this...

> [!TIP] > **We also have tips!**
>
> Tips are cool. Tips are like, "Hey here's a secret you didn't know!"
> Tips.

> [!WARNING]
>
> These originated from a band called Green Day.

> [!CAUTION]
>
> Caution, this caution is different to a Warning. Why? Who knows

> [!IMPORTANT]
>
> Important stuff is very important!

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

> **💭 Key Tip: Source Types**
>
> NotebookLM supports these source types:
>
> - Audio files
> - Copy and pasted text
> - Google Docs
> - Google Slides
> - Text, Markdown and PDF files
> - Web URLs
> - YouTube URLs of public videos
