# ReadOnlyVariable 

![image](ReadOnlyVariable_0.png)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<scxml xmlns="http://www.w3.org/2005/07/scxml" version="1.0" datamodel="ecmascript" name="ReadOnlyVariable">
	<datamodel>
		<data expr="0" id="myInt" />
		<data expr="'testString'" id="myString" />
		<data expr="true" id="myBool" />
		<data expr="1.1" id="myReal" />
		<data expr="0" id="A_myInt" />
		<data expr="'testString'" id="A_myString" />
		<data expr="true" id="A_myBool" />
		<data expr="1.1" id="A_myReal" />
	</datamodel>
	<state id="main_region">
		<initial>
			<transition target="StateA" type="internal" >
			</transition>
		</initial>
		<state id="StateB">
			<onentry>
				 <assign location="myInt" expr="100"/>
				 <assign location="myString" expr="'fail'"/>
				 <assign location="myBool" expr="false"/>
				 <assign location="myReal" expr="6.6"/>
				 <assign location="A_myInt" expr="200"/>
				 <assign location="A_myString" expr="'A_fail'"/>
				 <assign location="A_myBool" expr="false"/>
				 <assign location="A_myReal" expr="7.7"/>
			</onentry>
		</state>
		<state id="StateA">
			<transition event="ev"  target="StateB">
			</transition>
		</state>
	</state>
</scxml>
```
