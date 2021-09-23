---
title: <pattern>
slug: Web/SVG/Element/pattern
tags:
  - Element
  - SVG
  - SVG Container
browser-compat: svg.elements.pattern
---
<div>{{SVGRef}}</div>

<p>The <strong><code>&lt;pattern&gt;</code></strong> element defines a graphics object which can be redrawn at repeated x- and y-coordinate intervals ("tiled") to cover an area.</p>

<p>The <code>&lt;pattern&gt;</code> is referenced by the {{SVGAttr("fill")}} and/or {{SVGAttr("stroke")}} attributes on other <a href="/en-US/docs/Web/SVG/Tutorial/Basic_Shapes">graphics elements</a> to fill or stroke those elements with the referenced pattern.</p>

<h2>Example</h2>

<pre class="brush: css hidden">html,body,svg { height:100% }</pre>

<pre class="brush: html; highlight[4]">&lt;svg viewBox="0 0 230 100" xmlns="http://www.w3.org/2000/svg"&gt;
  &lt;defs&gt;
    &lt;pattern id="star" viewBox="0,0,10,10" width="10%" height="10%"&gt;
      &lt;polygon points="0,0 2,5 0,10 5,8 10,10 8,5 10,0 5,2"/&gt;
    &lt;/pattern&gt;
  &lt;/defs&gt;

  &lt;circle cx="50"  cy="50" r="50" fill="url(#star)"/&gt;
  &lt;circle cx="180" cy="50" r="40" fill="none" stroke-width="20" stroke="url(#star)"/&gt;
&lt;/svg&gt;</pre>

<p>{{EmbedLiveSample('Example', 150, '100%')}}</p>

<h2 id="Attributes">Attributes</h2>

<dl>
 <dt>{{SVGAttr("height")}}</dt>
 <dd>This attribute determines the height of the pattern tile.<br>
 <small><em>Value type</em>: <a href="/en-US/docs/Web/SVG/Content_type#length"><strong>&lt;length&gt;</strong></a>|<a href="/en-US/docs/Web/SVG/Content_type#percentage"><strong>&lt;percentage&gt;</strong></a>; <em>Default value</em>: <code>0</code>; <em>Animatable</em>: <strong>yes</strong></small></dd>
 <dt>{{SVGAttr("href")}}</dt>
 <dd>This attribute reference a template pattern that provides default values for the <code>&lt;pattern&gt;</code> attributes.<br>
 <small><em>Value type</em>: <a href="/en-US/docs/Web/SVG/Content_type#url"><strong>&lt;URL&gt;</strong></a>; <em>Default value</em>: <em>none</em>; <em>Animatable</em>: <strong>yes</strong></small></dd>
 <dt>{{SVGAttr("patternContentUnits")}}</dt>
 <dd>This attribute defines the coordinate system for the contents of the {{SVGElement("pattern")}}.<br>
 <small><em>Value type</em>: <code>userSpaceOnUse</code>|<code>objectBoundingBox</code>; <em>Default value</em>: <code>userSpaceOnUse</code>; <em>Animatable</em>: <strong>yes</strong></small>
 <div class="note"><p><strong>Note:</strong> This attribute has no effect if a <code>viewBox</code> attribute is specified on the <code>&lt;pattern&gt;</code> element.</p></div>
 </dd>
 <dt>{{SVGAttr("patternTransform")}}</dt>
 <dd>This attribute contains the definition of an optional additional transformation from the pattern coordinate system onto the target coordinate system.<br>
 <small><em>Value type</em>: <strong><a href="/en-US/docs/Web/SVG/Content_type#transform-list">&lt;transform-list&gt;</a></strong>; <em>Default value</em>: <em>none</em>; <em>Animatable</em>: <strong>yes</strong></small></dd>
 <dt>{{SVGAttr("patternUnits")}}</dt>
 <dd>This attribute defines the coordinate system for attributes <code>x</code>, <code>y</code>, <code>width</code> , and <code>height</code>.<br>
 <small><em>Value type</em>: <code>userSpaceOnUse</code>|<code>objectBoundingBox</code>; <em>Default value</em>: <code>objectBoundingBox</code>; <em>Animatable</em>: <strong>yes</strong></small></dd>
 <dt>{{SVGAttr("preserveAspectRatio")}}</dt>
 <dd>This attribute defines how the SVG fragment must be deformed if it is embedded in a container with a different aspect ratio.<br>
 <small><em>Value type</em>: (<code>none</code>| <code>xMinYMin</code>| <code>xMidYMin</code>| <code>xMaxYMin</code>| <code>xMinYMid</code>| <code>xMidYMid</code>| <code>xMaxYMid</code>| <code>xMinYMax</code>| <code>xMidYMax</code>| <code>xMaxYMax</code>) (<code>meet</code>|<code>slice</code>)? ; <em>Default value</em>: <code>xMidYMid meet</code>; <em>Animatable</em>: <strong>yes</strong></small></dd>
 <dt>{{SVGAttr("viewBox")}}</dt>
 <dd>This attribute defines the bound of the SVG viewport for the pattern fragment.<br>
 <small><em>Value type</em>: <strong><a href="/en-US/docs/Web/SVG/Content_type#list-of-ts">&lt;list-of-numbers&gt;</a></strong> ; <em>Default value</em>: none; <em>Animatable</em>: <strong>yes</strong></small></dd>
 <dt>{{SVGAttr("width")}}</dt>
 <dd>This attribute determines the width of the pattern tile.<br>
 <small><em>Value type</em>: <a href="/en-US/docs/Web/SVG/Content_type#length"><strong>&lt;length&gt;</strong></a>|<a href="/en-US/docs/Web/SVG/Content_type#percentage"><strong>&lt;percentage&gt;</strong></a> ; <em>Default value</em>: <code>0</code>; <em>Animatable</em>: <strong>yes</strong></small></dd>
 <dt>{{SVGAttr("x")}}</dt>
 <dd>This attribute determines the x coordinate shift of the pattern tile.<br>
 <small><em>Value type</em>: <a href="/en-US/docs/Web/SVG/Content_type#length"><strong>&lt;length&gt;</strong></a>|<a href="/en-US/docs/Web/SVG/Content_type#percentage"><strong>&lt;percentage&gt;</strong></a> ; <em>Default value</em>: <code>0</code>; <em>Animatable</em>: <strong>yes</strong></small></dd>
 <dt>{{SVGAttr("xlink:href")}} {{deprecated_inline}}</dt>
 <dd>This attribute reference a template pattern that provides default values for the <code>&lt;pattern&gt;</code> attributes.<br>
 <small><em>Value type</em>: <a href="/en-US/docs/Web/SVG/Content_type#url"><strong>&lt;URL&gt;</strong></a>; <em>Default value</em>: <em>none</em>; <em>Animatable</em>: <strong>yes</strong></small>
 <div class="note"><p><strong>Note:</strong> For browsers implementing <code>href</code>, if both <code>href</code> and <code>xlink:href</code> are set, <code>xlink:href</code> will be ignored and only <code>href</code> will be used.</p></div>
 </dd>
 <dt>{{SVGAttr("y")}}</dt>
 <dd>This attribute determines the y coordinate shift of the pattern tile.<br>
 <small><em>Value type</em>: <a href="/en-US/docs/Web/SVG/Content_type#length"><strong>&lt;length&gt;</strong></a>|<a href="/en-US/docs/Web/SVG/Content_type#percentage"><strong>&lt;percentage&gt;</strong></a> ; <em>Default value</em>: <code>0</code>; <em>Animatable</em>: <strong>yes</strong></small></dd>
</dl>

<h3 id="Global_attributes">Global attributes</h3>

<dl>
 <dt><a href="/en-US/docs/Web/SVG/Attribute/Core">Core Attributes</a></dt>
 <dd><small>Most notably: {{SVGAttr('id')}}, {{SVGAttr('tabindex')}}</small></dd>
 <dt><a href="/en-US/docs/Web/SVG/Attribute/Styling">Styling Attributes</a></dt>
 <dd><small>{{SVGAttr('class')}}, {{SVGAttr('style')}}</small></dd>
 <dt><a href="/en-US/docs/Web/SVG/Attribute/Conditional_Processing">Conditional Processing Attributes</a></dt>
 <dd><small>Most notably: {{SVGAttr('requiredExtensions')}}, {{SVGAttr('systemLanguage')}}</small></dd>
 <dt><a href="/en-US/docs/Web/SVG/Attribute/Presentation">Presentation Attributes</a></dt>
 <dd><small>Most notably: {{SVGAttr('clip-path')}}, {{SVGAttr('clip-rule')}}, {{SVGAttr('color')}}, {{SVGAttr('color-interpolation')}}, {{SVGAttr('color-rendering')}}, {{SVGAttr('cursor')}}, {{SVGAttr('display')}}, {{SVGAttr('fill')}}, {{SVGAttr('fill-opacity')}}, {{SVGAttr('fill-rule')}}, {{SVGAttr('filter')}}, {{SVGAttr('mask')}}, {{SVGAttr('opacity')}}, {{SVGAttr('pointer-events')}}, {{SVGAttr('shape-rendering')}}, {{SVGAttr('stroke')}}, {{SVGAttr('stroke-dasharray')}}, {{SVGAttr('stroke-dashoffset')}}, {{SVGAttr('stroke-linecap')}}, {{SVGAttr('stroke-linejoin')}}, {{SVGAttr('stroke-miterlimit')}}, {{SVGAttr('stroke-opacity')}}, {{SVGAttr('stroke-width')}}, {{SVGAttr("transform")}}, {{SVGAttr('vector-effect')}}, {{SVGAttr('visibility')}}</small></dd>
 <dt>XLink Attributes</dt>
 <dd><small>Most notably: {{SVGAttr("xlink:title")}}</small></dd>
</dl>

<h2 id="Usage_notes">Usage notes</h2>

<p>{{svginfo}}</p>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>