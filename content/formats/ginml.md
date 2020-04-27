---
title: "GINML"
date: 2014/10/31 09:37:11
summary: XML format used by GINsim
features: multivalued, documentation, layout
formats: ginml
---

The GINML format is an extension of the GXL (Graph eXchange Language) format.
It is mainly used for the definition of Logical Regulatory Graphs, but can also be used
to save State Transition Graphs.

GINML supports documentation, as well as layout information and styles.

In GINsim, the GINML file is usually part of a ZGINML archive, which can contain separate files
for associated information, such as perturbations or simulation parameters.

See http://doc.ginsim.org/format-zginml.html


# Sample


```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE gxl SYSTEM "http://ginsim.org/GINML_2_2.dtd">
<gxl xmlns:xlink="http://www.w3.org/1999/xlink">
  <graph class="regulatory" id="toy_3" nodeorder="G0 G1 G2">
  
    <nodestyle background="#ffffff" foreground="#000000" text="#000000" shape="RECTANGLE" width="45" height="25"/>
    <nodestyle background="#ffffff" foreground="#000000" text="#000000" shape="RECTANGLE" width="45" height="25"/>
    <edgestyle color="#000000" pattern="SIMPLE" line_width="1" properties="positive:#00c800 negative:#c80000 dual:#0000c8"/>
    <edgestyle color="#000000" pattern="SIMPLE" line_width="1" properties="positive:#00c800 negative:#c80000 dual:#0000c8"/>
    
    <node id="G0" maxvalue="1" input="true">
      <nodevisualsetting x="297" y="138" style=""/>
    </node>
    <node id="G1" maxvalue="1">
      <parameter idActiveInteractions=" G0:G1" val="1"/>
      <nodevisualsetting x="250" y="270" style=""/>
    </node>
    <node id="G2" maxvalue="1">
      <parameter idActiveInteractions=" G1:G2" val="1"/>
      <nodevisualsetting x="439" y="271" style=""/>
    </node>
    
    <edge id="G1:G2" from="G1" to="G2" minvalue="1" sign="positive" />
    <edge id="G0:G1" from="G0" to="G1" minvalue="1" sign="positive" />
    <edge id="G0:G2" from="G0" to="G2" minvalue="1" sign="negative" />
    
    <annotation>
      <linklist>
        <link xlink:href="www.ginsim.org"/>
      </linklist>
      <comment>Documentation can be added to the model itself, nodes, or edges</comment>
    </annotation>
  </graph>
</gxl>
```


