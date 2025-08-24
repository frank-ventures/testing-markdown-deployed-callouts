# testing-markdown-deployed-callouts
Let's see what different quote/callout blocks look like when deployed on Github pages.

## A quote block

> **Quotes!**
>
> This is a quote block.
>
> You may have seen them before. You can use them to, well, quote text.
>
> They get shown in this kinda grey font colour I don't really like. But not with some CSS applied!

In markdown you create quotes using a `>` character at the start of multiple lines. 

### Edit their style 
To edit the styling of **every** blockquote on a deployed GitHub page, you need an `assets/css/style.css` file. Target the `blockquote` HTML element and your styles will apply.

### Custom `blockquotes`

I guess if you want custom blockquotes on your deployed GitHub page (as in, ones which have different styling dependent on their content like the examples below) then you'd have to use HTML in your README file and use the `blockquote` element with CSS classes, combined with the stylesheet explained above.

## Notice blocks!

Woah, look at these guys!

Well actually, look at them in a GitHub repo because that's where you'll see their unique styling. On a deployed page they will not show up.

> [!NOTE]
> This is a note block. What does it look like when deployed? Well, if you're looking at it, it looks like this...

> [!TIP]
> **We also have tips!**
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
