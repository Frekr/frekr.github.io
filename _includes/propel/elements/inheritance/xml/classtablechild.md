~~~xml
<table name="book">
	<column name="id" type="integer" required="true" autoIncrement="true" primaryKey="true"/>
	<column name="cover" type="string"/>
	<unique name="IX_UQ_book_id">
		<unique-column name="id"/>
	</unique>
	<behavior name="delegate">
		<parameter name="to" value="itemRecord"/>
	</behavior>
</table>
~~~
