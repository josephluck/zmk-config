# ZMK Config

Wireless ergonomic split keyboard keymap config.

![keyboard](https://github.com/josephluck/zmk-config/blob/master/keyboard.jpg?raw=true)

## But why?

Using traditional keyboards (like the one on a MacBook) is uncomfortable for so many reasons:

- Traditional keyboards are in one piece, meaning your wrists and forearms must be bent in towards the center of your body, this is uncomfortable for wrists and shoulders after a prolonged period of time
- Key rows on a traditional keyboard aren't aligned vertically - this is a relic from old mechanical typewriters (can you believe it!?)
- Modifier keys (shift, control, alt, command etc) are usually towards the edges of the keyboard, which means you either use your weakest finger (pinky) to hold them down, or you use a stronger finger and awkwardly contort your hand to reach the secondary key. Over time this can cause significant discomfort
- Laptop and other more traditional keyboards use membrane or similar key switches which are optimised for cost and low-profile rather than comfort
- Laptop keyboards typically have around 66 keys at a minimum. You only have ten fingers so obviously each finger is responsible for covering a large number of keys, which means as lot of stretching away from their natural, most comfortable position

I'm a software engineer, which means I use my keyboard for very long periods, and I'm often accessing symbols and keyboard shortcuts. The combination of many of these highlighted problems led me to experience significant discomfort and pain after long typing sessions. Worried for the long term health of my wrists, shoulders and forearms (I had to take some time off from typing altogether at one stage!) I looked to improve my ergonomics by going down the rabbit hole of highly custom, ergonomic keyboards.

## Keyboard specs

- **34 keys** - Low number of keys minimises how much you need to move your fingers and wrist to access keys (34 keys is low enough that each key is no more than one key away from any finger, so very little stretching).
- **Split keyboard** - Allows each half of the keyboard to be placed under each wrist / forearm. This makes it much more comfortable for wrists and shoulders. Also forces you to use each the correct hand for each key.
- **Ortholinear staggered layout** - Keys are aligned in columns because your fingers don't move laterally when they bend (okay.. they do a little, but not by much). Each column is adjusted according to finger length (the pinky column is lower than the middle finger column for example), because why move your fingers to the keys when you can move the keys to your fingers?
- **Kailh low-profile switches** (gchoc, 20g springs, tape-modded and lubricated with Tribosys 3203) - These super-light switches are effortless to press, reducing fatigue on your fingers, especially when holding modifier keys
- **Black blank MBK keycaps** (o-ring modded) - This is personal choice, but with touch-typing you don't really need labels on each key
- **Nice!nano micro controllers** - Supports wireless firmware over bluetooth
- **Lithium ion rechargable batteries** - For wireless capability, tucked under the micro controller headers

## Keymap

- Two main layers, QWERTY and symbols
- Navigation layer for arrow keys
- Space and backspace on thumbs
- One-shot thumb key to access symbols layer
- Home-row mods for modifiers
