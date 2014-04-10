~~~xml
<table name="itemRecordHasAuthor" isCrossRef="true">
	<column name="bookId" type="integer" required="true" primaryKey="true"/>
	<column name="authorId" type="integer" required="true" primaryKey="true"/>
	<foreign-key foreignTable="author">
		<reference local="authorId" foreign="id"/>
	</foreign-key>
	<foreign-key foreignTable="itemRecord">
		<reference local="bookId" foreign="id"/>
	</foreign-key>
</table>
~~~
