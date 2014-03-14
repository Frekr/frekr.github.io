~~~xml
<many-to-one field="publisher" target-entity="publisher" 
inversed-by="itemRecord">
  <join-columns>
    <join-column name="publisherId" 
    referenced-column-name="id" 
    nullable="false"/>
  </join-columns>
</many-to-one>
~~~
