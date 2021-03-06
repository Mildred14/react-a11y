# img-uses-alt

Enforce that an `img` element contains the `alt` prop. The `alt` attribute specifies
an alternate text for an image, if the image cannot be displayed.


## options

*This rule takes no options*

## Passes

```js
// passes when the img has an `alt`
<img src="foo" alt="nice"/>

// passes when the img has an empty `alt` and role="presentation"
<img src="foo" alt="" role="presentation"/>

// passes when the img is aria-hidden
<img src="foo" aria-hidden="true"/>
```

## Fails

```js
// fails when the img doesn't have an `alt`
<img src="foo"/>

// fails when the img has alt="" but no role="presentation"
<img src="foo" alt=""/>
```

## See also

 - [This document](https://dequeuniversity.com/rules/axe/2.1/image-alt) from dequeuniversity.com
 - [This document](https://www.w3.org/WAI/PF/aria/roles#presentation) from w3.org
