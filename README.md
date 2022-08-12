# ZMK Config

Wireless ergonomic split keyboard keymap config.

![keyboard](https://github.com/josephluck/zmk-config/blob/master/keyboard.jpg?raw=true)

## But what's wrong with a "normal" keyboard?

Using traditional keyboards (like the one on a MacBook Pro) is uncomfortable for so many reasons:

#### Form factor

Most keyboards are in one piece, meaning your forearms tend to bend in towards the center of your body, and your wrists then bend outwards to reach the keys. This causes the muscles in your wrists to tense and is one of the most significant factors in causing discomfort after a prolonged period of typing.

#### Key position

The keys themselves aren't aligned in vertical rows. Look at the row `qwerty` compared to the row `asdfg`, the `asdfg` row starts to the right of `qwerty` (this is a relic from old mechanical typewriters can you believe it!?). This means that as you move your fingers down or up to reach a key, you also have to move left or right. Also, unless you train, it's likely that you don't use the "correct" finger for each key, because the misalignment of the key columns does not lend itself naturally to using the correct finger.

#### Modifier keys

Modifier keys (shift, control, alt, command etc) are usually towards the edges of the keyboard, which means you either use your weakest finger (pinky) to hold them down, or you use a stronger finger and awkwardly contort your hand to reach the secondary key. Over time this can cause significant discomfort.

#### Key switches

Laptop and other more traditional keyboards use membrane or similar key switches which are optimized for cost and low-profile rather than comfort. These switches are typically very low-profile, meaning that they do not have much cushioning as you press down. When the switch is activated, it feels more like a button than a smooth motion, which means that your finger pushes all the way to the bottom of the switch (until it can go no further) which might not seem that bad, but it tends to lead to smacking the keys on the keyboard rather than gently pushing them down. It can cause strain on the fingers.

#### Number of keys

Laptop keyboards typically have around 66 keys at a minimum. You only have ten fingers so obviously each finger is responsible for covering a large number of keys, which means as lot of stretching away from their natural position. Over time this additional movement can cause discomfort.

## So, what did it lead to?

I'm a software engineer, which means I use my keyboard for very long periods, and I'm often accessing symbols and keyboard shortcuts. The combination of many of these highlighted problems led me to experience significant discomfort and pain after long typing sessions. Worried for the long term health of my wrists, shoulders and forearms (I had to take some time off from typing altogether at one stage!) I looked to improve my ergonomics by going down the rabbit hole of highly custom, ergonomic keyboards.

## Keyboard specs

- **34 keys** - Low number of keys minimises how much you need to move your fingers and wrist to access keys (34 keys is low enough that each key is no more than one key away from any finger, so very little stretching).
- **Split keyboard** - Allows each half of the keyboard to be placed under each wrist / forearm. This makes it much more comfortable for wrists and shoulders. Also forces you to use each the correct hand for each key.
- **Ortholinear staggered layout** - Keys are aligned in columns because your fingers don't move laterally when they bend (okay.. they do a little, but not by much). Each column is adjusted according to finger length (the pinky column is lower than the middle finger column for example), because why move your fingers to the keys when you can move the keys to your fingers?
- **Kailh low-profile switches** (gchoc, 20g springs, tape-modded and lubricated with Tribosys 3203) - These super-light linear switches are effortless to press, reducing fatigue on your fingers, especially when holding modifier keys
- **Black blank MBK keycaps** (o-ring modded) - This is personal choice, but with touch-typing you don't really need labels on each key
- **Nice!nano micro controllers** - Supports wireless firmware over bluetooth
- **Lithium ion rechargable batteries** - For wireless capability, tucked under the micro controller headers

## Keymap

Keymaps are very personal things, but it's kinda fun to document my thought process. If you're embarking on your own crazy keyboard journey, I'd recommend experimenting with keymaps to find out what works well for you.

(note this keymap was created in QMK configurator, however the keymap is actually implemented using ZMK)

#### Features

- Two main layers, QWERTY and symbols
- Navigation layer for arrow keys
- Space and backspace on thumbs
- One-shot thumb key to access symbols layer
- Home-row mods for modifiers

#### Layer 0 (letters)

This layer is the main letters and common symbols layer. It also contains all the modifiers on the "home row" which is the four keys that your fingers naturally rest on. These modifiers are accessed by holding down the relevant key, and pressing the second key using the opposite hand (this is why the modifiers are mirrored on each side).

This layer also contains the space and backspace keys on the thumbs natural position. When either of these keys are held down, it activates the 2nd layer (see below) which contains the arrow keys. The secondary thumb key is a one-shot key to access the symbols layer. One-shot means that when activated, the symbols layer will be active until the next keypress, upon which the layer is deactivated and the letters layer is returned to. This means that to use a symbol, it's two keypresses rather than holding a modifier and pressing a letter/number.

![Keymap](https://github.com/josephluck/zmk-config/blob/master/layer-1.png?raw=true)

#### Layer 1 (symbols)

This layer contains all the symbols I need as a software engineer. It also contains the enter key on one of the thumbs. This might seem strange, but you don't actually type enter very often. It's a wonder why the enter key is so large on regular keyboards...

![Keymap](https://github.com/josephluck/zmk-config/blob/master/layer-2.png?raw=true)

#### Layer 2 (navigation)

This layer contains the arrow keys and is accessed by holding down one of the thumb keys. I use arrow key combos (i.e. navigate to the end of the line with `cmd+right`) and this keyboard layout fully supports any arrow combo by mirroring the modifier keys on all layers in the keymap.

This layer also contains the ZMK reset / bluetooth configuration keys, which are not captured in the keymap above.
