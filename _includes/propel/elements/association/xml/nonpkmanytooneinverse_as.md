~~~xml
<table name="publisher">
	<column name="id" primaryKey="true"/>
	<column name="name" type="string"/>
	<column name="vatCode" type="string" required="true"/>
	<unique name="IX_UQ_publisher_id">
		<unique-column name="id"/>
	</unique>
</table>
~~~