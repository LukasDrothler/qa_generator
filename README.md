# qa_generator

Dear reader,

thanks for your interest in our Question Answering System.

The Python script main.py contains all the code and has to be run for question-answer pair generation.

Inside the main function, the name or path of a Turtle (TTL) format ontology and a Configuration File is read in.

An ontology is a knowledge base which can be easily created with the Stanford Protégé tool.

The Configuration File format was created by us and it consists of multiple instances, that represent a group of Question-Answer pairs.

For your application of the Question Answering System, you need to create an own Configuration File in the following fashion:

Every instance starts with <INSTANCE>, ends with </INSTANCE>, contains a query,  associated question prototypes
and variables that allow to generate the same question with different values.

The section for a SPARQL query can be found between the keywords <QUERY> and </QUERY>.
It is important to note, that the variables used in the question are declared after SELECT and the result-variable comes last.

The selected variables will be returned in a table and while a variable contains the answer,
others will be part of the question, declared in the <QUESTION> section.
Questions have a static structure with dynamic entries, like 'When has John Doe birthday?' can be generated for 'When has ?firstname ?lastname birthday',
where ?fn = 'John' and ?ln = 'Doe'.

Lastly for the Python script to be able to create this kind of dynamic questions,
the used variables have to be declared in the <VARIABLES> area and important to note is,
that questions should not be provided with '?', because question marks will be created by the software.

Feel free to read my Bachelor's Thesis for further information.
