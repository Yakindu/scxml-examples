# EntryReactionAction 

![image](EntryReactionAction_0.png)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<scxml xmlns="http://www.w3.org/2005/07/scxml" version="1.0" datamodel="ecmascript" name="EntryReactionAction">
	<datamodel>
		<data expr="false" id="enteredR1" />
		<data expr="false" id="enteredR2" />
		<data expr="false" id="enteredBdefault" />
		<data expr="false" id="enteredBother" />
	</datamodel>
	<parallel>
	<state id="r2">
		<initial>
			<transition target="B" type="internal" >
			 <assign location="enteredR2" expr="true"/>
			</transition>
		</initial>
		<state id="B">
			<initial>
				<transition target="default" type="internal" >
				 <assign location="enteredBdefault" expr="true"/>
				</transition>
			</initial>
			<state id="BA">
				<transition event="b"  target="BB">
				</transition>
			</state>
			<history type = "shallow" id="default">
				<transition   target="BA">
					 <assign location="enteredBdefault" expr="true"/>
				</transition>
			</history>
			<state id="BB">
				<transition event="b"  target="BA">
				</transition>
			</state>
			<transition event="d"  target="D">
			</transition>
		</state>
		<state id="D">
			<transition event="b"  target="BB">
				 <assign location="enteredBother" expr="true"/>
			</transition>
			<transition event="d"  target="B">
			</transition>
		</state>
	</state>
	<state id="r1">
		<initial>
			<transition target="A" type="internal" >
			 <assign location="enteredR1" expr="true"/>
			</transition>
		</initial>
		<state id="A">
		</state>
	</state>
	</parallel>
</scxml>
```
