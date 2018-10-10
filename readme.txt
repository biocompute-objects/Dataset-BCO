Identification and Provenance fields
  Name: human_proteoform_glycosylation_sites_unicarbkb_glytoucan.csv
  Title: Glycosylation Sites (UniCarbKB)
  Created: Sept 9, 2018; 11:34:02
  Created by: Rahi Navelkar [rsn13@gwu.edu]
  Modified:    
  Modified by: 
  Digital Signature: RYFNNKE22594E007JKV457
  Verification status: Approved
  Publication status: Reviewed
  Authors: Matthew Campbell [m.campbell2@griffith.edu.au]; Robel Kahsay[rykahsay@email.gwu.edu ]; Rahi Navelkar [rsn13@gwu.edu]
  License: Data - Attribution 4.0 International CC BY 4.0 [https://creativecommons.org/licenses/by/4.0/]
	   Scripts - GNU General Public License v3.0 [https://www.gnu.org/licenses/gpl-3.0.en.html]

Usability Domain
  List of human [taxid:9606] proteins with information on glycosylation sites from UniCarbKB database [https://academic.oup.com/nar/article/42/D1/D215/1052197 ,https://doi.org/10.1093/nar/gkt1128]
 
Description Domain
  Description: This output file contains human [taxid:9606] proteins with information on glycosylation sites from UniCarbKB. The file also includes GlyTouCan accessions and UniCarbKB structure ids for associated glycan structures.
  Keywords: protein, canonical, glycosylation, glycan
  
  Pipeline steps:
    Step 1: The input file was retrieved directly from source.
    Step 2: The UniProt protein accessions in the input file were mapped to UniProt canonical accessions using a python script.
    Step 3: The glycosylation type (linkage type) was retrieved through UniCarbKB structure webpage using scripts [make-proteoform_glycosylation_sites_unicarbkb_glytoucan-csv-step2a.py, make-proteoform_glycosylation_sites_unicarbkb_glytoucan-csv-step2b.py]
    Step 4: The file was processed for quality check using a python script[make-proteoform_glycosylation_sites_unicarbkb_glytoucan-csv-step3.py]. Records which fall under one or more following criteria's are flagged and eliminated (eliminated records can be acessed using log file):
             a. If the protein accession is not included in UniProt protein list [UniProt Nov-2017 Release]
             b. If the amino acid position does not match to the amino acid on the associated position on fasta sequence [UniProt Nov-2017 Release]
             c. If the id (UnicarbKB structure id) is not present in input file.
             d. If the glycosylation type (linkage type) is not retrieved through step 3
             e. If a serine or threonine is reported for an N-linked glycan structure. 
             f. If an asparagine is reported for an O-linked glycan structure.

  Execution Domain:
  Script Location: https://github.com/glygener/glygen-backend/blob/master/integration/ 
  Scripts_list: make-proteoform_glycosylation_sites_unicarbkb_glytoucan-csv-step2a.py, make-proteoform_glycosylation_sites_unicarbkb_glytoucan-csv-step2b.py, make-proteoform_glycosylation_sites_unicarbkb_glytoucan-csv-step3.py
  Script Type: Text  
  Software Prerequisites:
    Name: Python
    Version: 2.7.13
    Name: Microsoft Excel
    Version: 14 or above

I/O Domain
  Input Subdomain: 
    name: human_protein_position_pmid_id_aminoacid_glytoucan_2018_09_04_07_51_27.txt
    mime-type: txt
    source/uri: http://data.glygen.org/datasets/source/human_protein_position_pmid_id_aminoacid_glytoucan_2018_09_04_07_51_27.txt

    name: human_protein_all.fasta
    mime-type: fasta
    source/uri:http://data.glygen.org/GLYDS00053
     
       
  Output Subdomain:
    name: human_proteoform_glycosylation_sites_unicarbkb_glytoucan.log
    mime-type: text
    source/uri: http://data.glygen.org/datasets/logs/human_proteoform_glycosylation_sites_unicarbkb_glytoucan.log

    name: human_proteoform_glycosylation_sites_unicarbkb_glytoucan.csv
    mime-type: csv
    source/uri: http://data.glygen.org/GLYDS00040

    Content:
      Column Headers:			
        uniprotkb_acc_canonical: Canonical protein accession from UniProt
        glycosylation_site: Glycosylation site on protein sequence
        evidence: Evidence (PMID) of the glycosylation
        uckb_id: UniCarbKB structure Id
        glytoucan_acc: Glycan accession from GlyTouCan database
        amino_acid: Three letter code abbreviation of amino acid
        glycosylation_type: Type of glycosylation (Linkage type)


	Statistics:
	        92 : uniprotkb_acc_canonical
	       223 : glycosylation_site
	       163 : evidence
	       984 : uckb_id
	       824 : glytoucan_acc
	         3 : amino_acid
	         3 : glycosylation_type