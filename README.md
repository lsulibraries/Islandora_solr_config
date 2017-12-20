# Combined date sort

This module provides a means to sort search results in Islandora based on date. A problem in the LDL instance of Islandora is that dates can be in different MODS fields, in particular <originInfo><dateCreated> and <originInfo><dateIssued>. Solr treats each of these fields as distinct fields. Furthermore, if there is an attribute (such as keyDate="yes", or qualifier="approximate"), then those fields are distinct from each other as well. By creating a solr field for the sort function that is copied and combined from the possible valid permutations, then we have a single field on which to hang our sorting hat.  


