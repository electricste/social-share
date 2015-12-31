# social-share

Social share widget supporting: wechat, weibo, linkedin, github, google+, rss, twitter, facebook and more.

Demo: http://harttle.com/social-share/

Dependencies [Fontawesome][font], [jQuery][jq].

## Usage

Import jQuery and Fontawesome:

```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css">
<script src="https://code.jquery.com/jquery-2.1.4.min.js"></script>
```

Import Social Share:

```html
<link rel="stylesheet" href="path/to/social-share.min.css">
<script src="path/to/social-share.min.js"></script>
```

Add script like this:

```javascript
var links = {
    facebook: {
        index: 2,
        url: 'https://www.facebook.com/harttle'
    },
    'google-plus': {
        index: 1,
        url: 'https://plus.google.com/+杨珺'
    },
    weibo: {
        index: 3,
        url: 'http://v.t.sina.com.cn/share/share.php?url=xxx&title=xxx&appid=xxx'
    },
    wechat: {
        index: 4,
        url: location.href
    },
    linkedin: {
        index: 5,
        url: 'https://linkedin.com/in/harttle'
    },
    rss: {
        url: 'http://harttle.com/feed.xml'
    },
    github: {
        url: 'https://github.com/harttle'
    },
    twitter: {
        url: 'https://twitter.com/harttleharttle'
    },
};

$('div').socialShare({ links: links, size: 'lg'});
```

## Options

### links

Type: `Object`

Default: `{}`

Share buttons are set in `links` object.

### size

Type: `String`

Default: `"md"`

Size of the buttons, available values: 

* `"lg"`(large)
* `"md"`(medium)
* `"sm"`(small)
* `"xs"`(exteme small)

### blank

Type: `Boolean`

Default: `true`

Should the links open in new window? If set `true`, `target="_blank"` will be set.

## links.url

Type: `String`

The `href` attribute for the the share button. For `"wechat"`, `links.url` is the url encoded within the qrcode img.

## links.index

Type: `Number`

Optional, share buttons are sorted by `links.index`.


[font]: http://fontawesome.io/
[jq]: http://jquery.com/