# ConditionalExpressions 

![image](ConditionalExpressions_0.png)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<scxml xmlns="http://www.w3.org/2005/07/scxml" version="1.0" datamodel="ecmascript" name="ConditionalExpressions">
	<datamodel>
		<data expr="boolVar ? 3 : 2" id="condition" />
		<data expr="true" id="boolVar" />
		<data expr="''" id="stringVar" />
		<data expr="''" id="stringCondition" />
	</datamodel>
	<state id="main_region">
		<initial>
			<transition target="A" type="internal" >
			</transition>
		</initial>
		<state id="A">
			<onentry>
				 <assign location="condition" expr="boolVar ? 1 : 0"/>
			</onentry>
			<transition event="e" cond="1 == (boolVar ? 1 : 0)" target="B">
			</transition>
		</state>
		<state id="B">
			<onentry>
				 <assign location="condition" expr="((condition == 2) ? 1 : 2)"/>
				 <assign location="stringCondition" expr="((condition == 2) ? 'True' : 'False')"/>
			</onentry>
		</state>
	</state>
</scxml>
```
