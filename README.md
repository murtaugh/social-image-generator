# A dynamic social image generator

If your content doesn't naturally come with imagery for social media cards, generate one from the text of the content. Easy to hook up to any CMS, just output an entry's title and description into the right spots and voila.

All the text areas are `contenteditable` so you can tweak the preview before generating the image.

## Notes

1. The <a href="https://html2canvas.hertzen.com">html2canvas</a> script is needed, which is limited in the CSS properties it can handle.
2. It defaults to the same 1200x600 size that GitHub itself defaults to.
3. The preview card needs to be fully in the viewport in order for html2canvas to be successful.
4. Images can be tricky: I haven't successfully gotten a BG image to render, and the one SVG I've tried so far needed to be manually given the height and width I wanted. The height and width defined in the SVG itself was overriding any sizes I tried to give it via CSS.
5. WordPress has this feature built in to Jetpack, but it uses a headless browser on the server to do the rendering. This allows it to generate and save the images all programmatically, but I can't be bothered. Until I harden the dseign to work in any circumstance, I'll want to preview the iages anyway.
