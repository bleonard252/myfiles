---
title: Cards
---
Cards are snippets of data or controls that display on supported viewers. Examples include media players, Now Playing information, profile embeds, or announcements. Although you could use myfile cards for posts, it's best to use a proper social platform, such as [Mastodon](https://joinmastodon.org), for your posts instead of cards. Some types of cards use the `type` field, while others use three basic fields for content.

## Cards with title and content
The most basic type of card does not include the `type` field, but instead uses `title` and one or both of `text` or `image`. Examples are below:

```json
{
    "title": "This will show in big, bold letters above the text!",
    "text": "This will show in normal letters below the title."
}
```
```json
{
    "title": "A picture of my cat",
    "image": "https://purr.objects-us-east-1.dream.io/i/pushkincropped.jpg",
    "text": "Isn't that cat just awesome?"
}
```