### Chat bubble
Chat bubbles are used to show one line of conversation and all its data, including the author image, author name, and time.

[Chat bubble documentation](https://v4.daisyui.com/components/chat/)

#### Class names
- component: `chat`, `chat-image`, `chat-header`, `chat-footer`, `chat-bubble`
- color: `chat-bubble-primary`, `chat-bubble-secondary`, `chat-bubble-accent`, `chat-bubble-info`, `chat-bubble-success`, `chat-bubble-warning`, `chat-bubble-error`
- modifier: `chat-start`, `chat-end`

#### Syntax
```html
<div class="chat chat-start">
  <div class="chat-image avatar"></div>
  <div class="chat-bubble">Hello</div>
</div>
```
#### Rules
- `chat-start` / `chat-end` set the sender side.
- Structure: `chat-image` + `chat-header` + `chat-footer` + `chat-bubble`, and add a bubble color (`chat-bubble-primary`).
