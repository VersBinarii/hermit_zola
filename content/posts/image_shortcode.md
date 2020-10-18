+++
title = 'The "image" Shortcode'
date = 2018-12-24T12:29:41+08:00
draft = false
[taxonomies]
tags=["demo", "image"]
+++

This theme has `image` shortcode built in, documentations can be found here:

https://github.com/pawndev/hermit_zola/#image

This shortcode provider this API for image:

- src: The url of the image
- class: You can apply class to the current img
- alt: The alt of the image
- style: Custom CSS style to apply on the img element

Here's an example:

{{ image(src="https://via.placeholder.com/1600x800", alt="Hello Friend", style="border-radius: 8px;") }}

Suspendisse fringilla malesuada massa, in malesuada orci lacinia a. Praesent dapibus faucibus nisl, id volutpat elit bibendum eu. Nulla vitae laoreet nibh, eu hendrerit lacus. Donec lacinia auctor ligula, vel interdum ipsum malesuada vitae. Donec placerat a justo eu gravida. Aenean ultricies imperdiet convallis. Pellentesque accumsan non ex sed euismod. Proin bibendum lectus nec enim faucibus feugiat. Donec hendrerit nisi viverra ornare luctus. Nullam non viverra nisl. Nam vel tellus et tortor elementum volutpat sit amet et erat. Aliquam a libero quis libero porta consectetur. Etiam aliquam felis vel nulla mattis finibus. Mauris laoreet lacus arcu, sed rhoncus odio condimentum sed. Aenean in dui rutrum elit faucibus faucibus nec fringilla augue. Fusce non ornare mauris.

Pellentesque eu consequat nunc. Vivamus eu eros ut nulla dapibus molestie in id tortor. Cras viverra ligula erat, tincidunt hendrerit diam blandit nec. Cras id urna vel dolor dictum mattis. Vestibulum congue erat ac eros molestie accumsan. Maecenas lorem nibh, maximus vel justo eget, facilisis egestas lectus. Mauris eu est ut odio blandit consequat id feugiat eros. Fusce id suscipit mi, et lacinia lectus. Mauris a arcu placerat dolor iaculis feugiat nec non mi. Ut porttitor elit tortor, eget tempus velit mollis eu. Aliquam sem nulla, dictum cursus mauris ac, semper ullamcorper leo.

Donec nec tincidunt est. Sed id metus in erat fringilla mattis at id turpis. Aliquam tempor vehicula faucibus. Phasellus consequat aliquam odio. Morbi a ex vitae sapien porta auctor. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec sit amet nulla arcu. Praesent ut tortor purus. Praesent id eros diam. Pellentesque vitae dolor at nibh ultrices accumsan eu id urna. Aliquam finibus interdum orci in varius. Pellentesque a enim condimentum, condimentum felis id, vehicula augue. Vivamus cursus commodo eros nec lacinia.
