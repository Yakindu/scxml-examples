# TransitionGuardedTimeTrigger 

![image](TransitionGuardedTimeTrigger_0.png)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<scxml xmlns="http://www.w3.org/2005/07/scxml" version="1.0" datamodel="ecmascript" name="TransitionGuardedTimeTrigger">
	<datamodel>
		<data expr="0" id="x" />
	</datamodel>
	<state id="main_region">
		<initial>
			<transition target="A" type="internal" >
			</transition>
		</initial>
		<state id="A">
			<onentry>
				<send event="A_t_0_timeEvent_0" delay="1s"/>
			</onentry>
			<onexit>
				<cancel sendid="A_t_0_timeEvent_0" />
			</onexit>
			<transition event="A_t_0_timeEvent_0" cond="x == 0" target="B">
				 <assign location="x" expr="x + 1"/>
			</transition>
		</state>
		<state id="B">
		</state>
	</state>
</scxml>
```
