# Constants 

![image](Constants_0.png)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<scxml xmlns="http://www.w3.org/2005/07/scxml" version="1.0" datamodel="ecmascript" name="Constants">
	<datamodel>
		<data expr="10" id="x" />
		<data expr="x * 2" id="y" />
		<data expr="0" id="result" />
		<data expr="'Hello World'" id="Named_y" />
		<data expr="2" id="Named_two" />
		<data expr="5" id="internalConstant" />
	</datamodel>
	<state id="main_region">
		<initial>
			<transition target="A" type="internal" >
			</transition>
		</initial>
		<state id="A">
			<transition event="e"  target="B">
			</transition>
		</state>
		<state id="B">
			<onentry>
				 <assign location="result" expr="Named_two * x"/>
			</onentry>
			<transition event="e3"  target="C">
			</transition>
		</state>
		<state id="C">
			<onentry>
				 <assign location="result" expr="result * internalConstant"/>
			</onentry>
			<transition event="e2"  target="A">
				 <assign location="result" expr="_event.data * x * Named_two * internalConstant"/>
			</transition>
		</state>
	</state>
</scxml>
```
