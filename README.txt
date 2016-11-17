PUBLICO 1994 QUOTATION ATTRIBUTION CORPUS (QUAC), v1.0
15 April 2014


1) General Information

This file consists on a dataset for Quotation Attribution on Portuguese news, created within the scope of my Master thesis [1]. 
The original documents consist in 100 000 unmarked news from the Portuguese newspaper “PUBLICO” (1994). 

From that, a fraction of the original corpus was manually annotated yielding a total of 212 annotated news and 971 annotated quotes. The steps taken to obtain the final corpus were the following:
--	Tokenization;
--	Named Entity Recognition;
--	Part-of-Speech tagging and parsing; 
--	Automatic identification of quotes;
--	Manual annotation of coreferences and partial coreference resolution;
--	Manual author attribution.

For more information, please refer to Chapter 4 of [1]. 

If you use this corpus in your research, please cite the following work:
[1] Quintão, Marta E.(2014). Quotation Attribution for Portuguese News Corpora. M.Sc. Thesis. Técnico Lisboa/UTL: Portugal.

For any questions or comments, please send email to <marta.pereira.quintao@tecnico.ulisboa.pt>.


2) File Structure

In the main folder you will find this README alongside an XML file with the annotated corpus. 
The file contains the set of annotated news articles, one for each <doc> tag, with attributes containing the news index "num, the news day "newsday", and the index for the news day in "newsdaynum". 
-- If no quotes were found on the news article then no authors are marked and an attribute "condition" is set to "No_Quotes_Found". 
-- If the news article is a summary then an attribute "type" is added and set to "RES".
-- If the news article is an interview then an attribute "type" is added and set to "ENT".

Each <doc> tag includes the complete news article in <text>, followed by the tokenized text in <tokenized_text>. The tags <paragraph>, <sentence> and <word> mark the structure of the text. To the <word> tag, the attributes in "self", “POStag”, “parent” and “dependency” were assigned with the corresponding information of its dependency tree and part-of-speech tagging.

The authors in the text are marked with a <author> tag and the attributes "authorID" and "alternativeID", storing information on the authors unique ID the unique ID of its older coreference respectively. If no coreferences exist in the news article, the the value for the attribute "alternativeID" is set to N/A.
-- If the author was manually added, an attribute "added" is added and set to "True".
-- If the author was manually modified from its automatic detection, an attribute "altered" is added and set to "True".

The quotes are marked with a <quote> tag and the attributes "authorID" and "quoteID", storing information on the ID of its assigned author and the quotes unique ID respectively.
-- If the quote was manually added, an attribute "added" is added and set to "True".
-- If the quote was manually modified from its automatic detection, an attribute "altered" is added and set to "True".

For more information, please refer to Chapter 4 of the document of the thesis “Quotation Attribution for Portuguese News Corpora”. 


3) License

PUBLICO 1994 Quotation Attribution Corpus (c) by Marta Quintão

PUBLICO 1994 Quotation Attribution Corpus is owned by Marta Quintão and licensed under the Creative Commons Attribution-ShareAlike 4.0 International License.
You should have received a copy of the license along with this work. If not, see <http://creativecommons.org/licenses/by-sa/4.0/>. 


4) Acknowledgements

The original (unmarked news) dataset CHAVE was compiled within the CLEF initiative by Linguateca <http://www.linguateca.pt> and is available at <http://www.linguateca.pt/CHAVE/>. It contains news from de newspapers "Público" <http://www.publico.pt> and  "Folha de São Paulo" <http://www.folha.com.br> for the years 1994 and 1995. 

I would like to thank Priberam for providing the news articles and supporting the M.Sc. thesis which lead to the creation of this corpus and, in particular, to André F. T. Martins, Miguel B. Almeida, Prof. Mário Figueiredo (supervisors of the M.Sc. thesis) and Mariana S. C. Almeida for helping and providing the necessary tools.
