## ISO 19115 xml metadata generator Module

This java module is used to generate iso19115 metadata for nccp monthly aggregated data fomr the plain text metadata files.

To build the module: `mvn clean compile assembly:single`. It will create an executable jar called `iso19115-xml-gen.jar`.

A `defaluts.properties` file should be present in the execution directory to run the executable jar.

To run the executable jar: `java -jar iso19115-xml-gen.jar -indir indir -infileext ext -outdir outdir -lines numlines`

Example: `java -jar iso19115-xml-gen.jar -indir /home/mdmoinulh/nrdc_dataone/raw_data -infileext csv -outdir /home/mdmoinulh/nrdc_dataone/raw_data -lines 10`


The jar creates **iso19115 xml** for each of the file in the **indir** (with extension **infileext**) to the output dir **outdir**. I t assumes first n lines (specified with **lines** argument) of the input file contains metadata of the file
