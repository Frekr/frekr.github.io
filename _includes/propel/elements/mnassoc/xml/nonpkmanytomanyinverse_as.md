~~~xml
<table name="author">
	<column name="id" primaryKey="true"/>
	<column name="firstName" type="string" required="true"/>
	<column name="lastName" type="string" required="true"/>
	<unique name="IX_UQ_author_id">
		<unique-column name="id"/>
	</unique>
</table>
~~~