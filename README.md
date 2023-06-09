# TIBCO BusinessWorks 5.X - Split Large XML File
<p>
<img src =https://img.shields.io/static/v1?label=licence&message=MIT&color=green />
</p>
<p>This proof of concept demonstrates how to split an XML file into smaller parts with a pre-defined number of elements per node, without using plugins.</p>

### Example

<p>To exemplify the operation, the following XML file was used, and the number of elements per node was defined as <strong>3</strong> in <strong>GV BW_SPLIT_LARGE_XML/nodeSize</strong></p>

      <?xml version = "1.0" encoding = "UTF-8"?>
      <ns0:employees xmlns:ns0="http://www.tibco.com/schemas/BW5_SPLIT_LARGE_XML/Shared Resources/Schemas/Schema.xsd">
	      <ns0:employee>
		      <ns0:id>1</ns0:id>
		      <ns0:firstName>Jose</ns0:firstName>
		      <ns0:lastName>Silva</ns0:lastName>
		      <ns0:email>jose.silva@email.com</ns0:email>
	      </ns0:employee>
	      <ns0:employee>
		      <ns0:id>2</ns0:id>
		      <ns0:firstName>Mariana</ns0:firstName>
		      <ns0:lastName>Leal</ns0:lastName>
		      <ns0:email>mariana.leal@email.com</ns0:email>
	      </ns0:employee>
	      <ns0:employee>
		      <ns0:id>3</ns0:id>
		      <ns0:firstName>Patricia</ns0:firstName>
		      <ns0:lastName>Lima</ns0:lastName>
		      <ns0:email>patricia.lima@email.com</ns0:email>
	      </ns0:employee>
	      <ns0:employee>
		      <ns0:id>4</ns0:id>
		      <ns0:firstName>Lucas</ns0:firstName>
		      <ns0:lastName>Machado</ns0:lastName>
		      <ns0:email>lucas.machado@email.com</ns0:email>
	      </ns0:employee>
	      <ns0:employee>
		      <ns0:id>5</ns0:id>
		      <ns0:firstName>Carlos</ns0:firstName>
		      <ns0:lastName>Cardoso</ns0:lastName>
		      <ns0:email>carlos.cardoso@email.com</ns0:email>
	      </ns0:employee>
	      <ns0:employee>
		      <ns0:id>6</ns0:id>
		      <ns0:firstName>Naiara</ns0:firstName>
		      <ns0:lastName>Campos</ns0:lastName>
		      <ns0:email>naiara.campos@email.com</ns0:email>
	      </ns0:employee>
	      <ns0:employee>
		      <ns0:id>7</ns0:id>
		      <ns0:firstName>Manoel</ns0:firstName>
		      <ns0:lastName>Oliveira</ns0:lastName>
		      <ns0:email>manoel.oliveira@email.com</ns0:email>
	      </ns0:employee>
	      <ns0:employee>
		      <ns0:id>8</ns0:id>
		      <ns0:firstName>Lucia</ns0:firstName>
		      <ns0:lastName>Franco</ns0:lastName>
		      <ns0:email>lucia.franco@email.com</ns0:email>
	      </ns0:employee>
       </ns0:employees>
       
<p>The execution of the process will generate 3 XML files, as shown in the examples below.</p>

##### Output XML 01

	<?xml version = "1.0" encoding = "UTF-8"?>
	<ns0:employees xmlns:ns0 = "http://www.tibco.com/schemas/BW5_SPLIT_LARGE_XML/Shared Resources/Schemas/Schema.xsd">
		<ns0:employee>
			<ns0:id>1</ns0:id>
			<ns0:firstName>Jose</ns0:firstName>
			<ns0:lastName>Silva</ns0:lastName>
			<ns0:email>jose.silva@email.com</ns0:email>
		</ns0:employee>
		<ns0:employee>
			<ns0:id>2</ns0:id>
			<ns0:firstName>Mariana</ns0:firstName>
			<ns0:lastName>Leal</ns0:lastName>
			<ns0:email>mariana.leal@email.com</ns0:email>
		</ns0:employee>
		<ns0:employee>
			<ns0:id>3</ns0:id>
			<ns0:firstName>Patricia</ns0:firstName>
			<ns0:lastName>Lima</ns0:lastName>
			<ns0:email>patricia.lima@email.com</ns0:email>
		</ns0:employee>
	</ns0:employees>

##### Output XML 02

	<?xml version = "1.0" encoding = "UTF-8"?>
	<ns0:employees xmlns:ns0 = "http://www.tibco.com/schemas/BW5_SPLIT_LARGE_XML/Shared Resources/Schemas/Schema.xsd">
		<ns0:employee>
			<ns0:id>4</ns0:id>
			<ns0:firstName>Lucas</ns0:firstName>
			<ns0:lastName>Machado</ns0:lastName>
			<ns0:email>lucas.machado@email.com</ns0:email>
		</ns0:employee>
		<ns0:employee>
			<ns0:id>5</ns0:id>
			<ns0:firstName>Carlos</ns0:firstName>
			<ns0:lastName>Cardoso</ns0:lastName>
			<ns0:email>carlos.cardoso@email.com</ns0:email>
		</ns0:employee>
		<ns0:employee>
			<ns0:id>6</ns0:id>
			<ns0:firstName>Naiara</ns0:firstName>
			<ns0:lastName>Campos</ns0:lastName>
			<ns0:email>naiara.campos@email.com</ns0:email>
		</ns0:employee>
	</ns0:employees>
	
##### Output XML 03

	<?xml version = "1.0" encoding = "UTF-8"?>
	<ns0:employees xmlns:ns0 = "http://www.tibco.com/schemas/BW5_SPLIT_LARGE_XML/Shared Resources/Schemas/Schema.xsd">
		<ns0:employee>
			<ns0:id>7</ns0:id>
			<ns0:firstName>Manoel</ns0:firstName>
			<ns0:lastName>Oliveira</ns0:lastName>
			<ns0:email>manoel.oliveira@email.com</ns0:email>
		</ns0:employee>
		<ns0:employee>
			<ns0:id>8</ns0:id>
			<ns0:firstName>Lucia</ns0:firstName>
			<ns0:lastName>Franco</ns0:lastName>
			<ns0:email>lucia.franco@email.com</ns0:email>
		</ns0:employee>
	</ns0:employees>
