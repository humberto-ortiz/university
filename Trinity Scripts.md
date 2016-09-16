INDIVIDUAL ASSEMBLY:

SCRIPT 1:

#!/bin/bash
#$ -S /bin/bash
#$ -N Trinity
#$ -M david.ortiz11@upr.edu 
#$ -m es
#$ -cwd
#$ -pe orte 1
##

Trinity --seqType fq --max_memory 50G --left /storage/home/dortiz/Stygichthys/ER1_ACAGTG_L002_R1_001.fastq,/storage/home/dortiz/Stygichthys/Mo1_CGATGT_L002_R1_001.fastq,/storage/home/dortiz/Stygichthys/NC1_ATGTCA_L002_R1_001.fastq,/storage/home/dortiz/Stygichthys/SK1_AGTCAA_L002_R1_001.fastq --right /storage/home/dortiz/Stygichthys/ER1_ACAGTG_L002_R2_001.fastq,/storage/home/dortiz/Stygichthys/Mo1_CGATGT_L002_R2_001.fastq,/storage/home/dortiz/Stygichthys/NC1_ATGTCA_L002_R2_001.fastq,/storage/home/dortiz/Stygichthys/SK1_AGTCAA_L002_R2_001.fastq --SS_lib_type RF --CPU 5 --normalize_by_read_set --no_bowtie --output /storage/home/dortiz/Stygichthys/Individuos/trinityIndividuo01

SCRIPT 2:

#!/bin/bash
#$ -S /bin/bash
#$ -N Trinity
#$ -M david.ortiz11@upr.edu 
#$ -m es
#$ -cwd
#$ -pe orte 1
##

Trinity --seqType fq --max_memory 50G --left /storage/home/dortiz/Stygichthys/ER2_GCCAAT_L002_R1_001.fastq, /storage/home/dortiz/Stygichthys/NC2_CCGTCC_L002_R1_001.fastq, /storage/home/dortiz/Stygichthys/SK2_TGACCA_L002_R1_001.fastq --right /storage/home/dortiz/Stygichthys/ER2_GCCAAT_L002_R2_001.fastq, /storage/home/dortiz/Stygichthys/NC2_CCGTCC_L002_R2_001.fastq, /storage/home/dortiz/Stygichthys/SK2_TGACCA_L002_R2_001.fastq --SS_lib_type RF --CPU 2 --normalize_max_read_cov --no_bowtie --output /storage/home/dortiz/Stygichthys/Individuostrinity/Individuo02

SCRIPT 3:

#!/bin/bash
#$ -S /bin/bash
#$ -N Trinity
#$ -M david.ortiz11@upr.edu 
#$ -m es
#$ -cwd
#$ -pe orte 1
##

Trinity --seqType fq --max_memory 50G --left /storage/home/dortiz/Stygichthys/ER3_CAGATC_L002_R1_001.fastq, /storage/home/dortiz/Stygichthys/Mo3_CTTGTA_L002_R1_001.fastq, /storage/home/dortiz/Stygichthys/
NC3_GTCCGC_L002_R1_001.fastq, /storage/home/dortiz/Stygichthys/
SK3_AGTTCC_L002_R1_001.fastq --right /storage/home/dortiz/Stygichthys/ER3_CAGATC_L002_R2_001.fastq, /storage/home/dortiz/Stygichthys/Mo3_CTTGTA_L002_R2_001.fastq, /storage/home/dortiz/Stygichthys/NC3_GTCCGC_L002_R2_001.fastq, /storage/home/dortiz/Stygichthys/SK3_AGTTCC_L002_R2_001.fastq --SS_lib_type RF --CPU 2 --normalize_max_read_cov --no_bowtie --output /storage/home/dortiz/Stygichthys/Individuostrinity/Individuo03

REFERENCE SCRIPT:

#!/bin/bash
#$ -S /bin/bash
#$ -N Trinity
#$ -M david.ortiz11@upr.edu 
#$ -m es
#$ -cwd
#$ -pe orte 1
##

module load trinity/v2.0.6

perl /c1/apps/trinity/trinityrnaseq-2.0.6/Trinity --seqType fq --max_memory 50G --left /home/arcilame/NEW_Transcriptomics_Fish/Trim_Reverse_R2.fastq --right /home/arcilame/NEW_Transcriptomics_Fish/Trim_Forward_R1.fastq --SS_lib_type RF --CPU 16 --normalize_reads --output /home/arcilame/NEW_Transcriptomics_Fish/TrinityCavefish_onlytrim

DIRECTORY:

/storage/home/dortiz/Stygichthys


FILES:

ER1_ACAGTG_L002_R1_001.fastq  ER1_ACAGTG_L002_R2_001.fastq
ER2_GCCAAT_L002_R1_001.fastq  ER2_GCCAAT_L002_R2_001.fastq
ER3_CAGATC_L002_R1_001.fastq  ER3_CAGATC_L002_R2_001.fastq

Mo1_CGATGT_L002_R1_001.fastq  Mo1_CGATGT_L002_R2_001.fastq
Mo3_CTTGTA_L002_R1_001.fastq  Mo3_CTTGTA_L002_R2_001.fastq 

NC1_ATGTCA_L002_R1_001.fastq  NC1_ATGTCA_L002_R2_001.fastq
NC2_CCGTCC_L002_R1_001.fastq  NC2_CCGTCC_L002_R2_001.fastq
NC3_GTCCGC_L002_R1_001.fastq  NC3_GTCCGC_L002_R2_001.fastq
 
SK1_AGTCAA_L002_R1_001.fastq  SK1_AGTCAA_L002_R2_001.fastq
SK2_TGACCA_L002_R1_001.fastq  SK2_TGACCA_L002_R2_001.fastq
SK3_AGTTCC_L002_R1_001.fastq  SK3_AGTTCC_L002_R2_001.fastq

///////////////////////////////////////////////////////////////////
																//
TISSUE ASSEMBLY:

SCRIPT 1:

#!/bin/bash
#$ -S /bin/bash
#$ -N Trinity
#$ -M david.ortiz11@upr.edu 
#$ -m es
#$ -cwd
#$ -pe orte 5
##

Trinity --seqType fq --max_memory 60G --no_bowtie --left /storage/home/dortiz/Stygichthys/ER1_ACAGTG_L002_R1_001.fastq,/storage/home/dortiz/Stygichthys/ER2_GCCAAT_L002_R1_001.fastq,/storage/home/dortiz/Stygichthys/ER3_CAGATC_L002_R1_001.fastq --right /storage/home/dortiz/Stygichthys/ER1_ACAGTG_L002_R2_001.fastq,/storage/home/dortiz/Stygichthys/ER2_GCCAAT_L002_R2_001.fastq,/storage/home/dortiz/Stygichthys/ER3_CAGATC_L002_R2_001.fastq --SS_lib_type RF --CPU 5 --normalize_by_read_set --output /storage/home/dortiz/Stygichthys/Tejido/trinityTejido01

SCRIPT 2:

#!/bin/bash
#$ -S /bin/bash
#$ -N Trinity
#$ -M david.ortiz11@upr.edu 
#$ -m es
#$ -cwd
#$ -pe orte 1
##

Trinity --seqType fq --max_memory 50G --left /storage/home/dortiz/Stygichthys/Mo1_CGATGT_L002_R1_001.fastq, /storage/home/dortiz/Stygichthys/Mo3_CTTGTA_L002_R1_001.fastq --right /storage/home/dortiz/Stygichthys/Mo1_CGATGT_L002_R2_001.fastq, /storage/home/dortiz/Stygichthys/Mo3_CTTGTA_L002_R2_001.fastq --SS_lib_type RF --CPU 2 --normalize_by_read_set --no_bowtie --output /storage/home/dortiz/Stygichthys/Tejido/trinityTejido02

SCRIPT 3:

#!/bin/bash
#$ -S /bin/bash
#$ -N Trinity
#$ -M david.ortiz11@upr.edu 
#$ -m es
#$ -cwd
#$ -pe orte 1
##

Trinity --seqType fq --max_memory 50G --left /storage/home/dortiz/Stygichthys/NC1_ATGTCA_L002_R1_001.fastq, /storage/home/dortiz/Stygichthys/NC2_CCGTCC_L002_R1_001.fastq, /storage/home/dortiz/Stygichthys/
NC3_GTCCGC_L002_R1_001.fastq --right /storage/home/dortiz/Stygichthys/NC1_ATGTCA_L002_R2_001.fastq, /storage/home/dortiz/Stygichthys/NC2_CCGTCC_L002_R2_001.fastq, /storage/home/dortiz/Stygichthys/NC3_GTCCGC_L002_R2_001.fastq --SS_lib_type RF --CPU 2 --normalize_by_read_set --no_bowtie --output /storage/home/dortiz/Stygichthys/Tejido/trinityTejido03

SCRIPT 4:

#!/bin/bash
#$ -S /bin/bash
#$ -N Trinity
#$ -M david.ortiz11@upr.edu 
#$ -m es
#$ -cwd
#$ -pe orte 1
##

Trinity --seqType fq --max_memory 50G --left /storage/home/dortiz/Stygichthys/SK1_AGTCAA_L002_R1_001.fastq, /storage/home/dortiz/Stygichthys/SK2_TGACCA_L002_R1_001.fastq, /storage/home/dortiz/Stygichthys/SK3_AGTTCC_L002_R1_001.fastq --right /storage/home/dortiz/Stygichthys/SK1_AGTCAA_L002_R2_001.fastq, /storage/home/dortiz/Stygichthys/  SK2_TGACCA_L002_R2_001.fastq, /storage/home/dortiz/Stygichthys/SK3_AGTTCC_L002_R2_001.fastq --SS_lib_type RF --CPU 2 --normalize_by_read_set --no_bowtie --output /storage/home/dortiz/Stygichthys/Tejido/trinityTejido04

REFERENCE SCRIPT:

#!/bin/bash
#$ -S /bin/bash
#$ -N Trinity
#$ -M david.ortiz11@upr.edu 
#$ -m es
#$ -cwd
#$ -pe orte 1
##

module load trinity/v2.0.6

perl /c1/apps/trinity/trinityrnaseq-2.0.6/Trinity --seqType fq --max_memory 50G --left /home/arcilame/NEW_Transcriptomics_Fish/Trim_Reverse_R2.fastq --right /home/arcilame/NEW_Transcriptomics_Fish/Trim_Forward_R1.fastq --SS_lib_type RF --CPU 16 --normalize_reads --output /home/arcilame/NEW_Transcriptomics_Fish/TrinityCavefish_onlytrim

DIRECTORY:

/storage/home/dortiz/Stygichthys


FILES:

ER1_ACAGTG_L002_R1_001.fastq  ER1_ACAGTG_L002_R2_001.fastq
ER2_GCCAAT_L002_R1_001.fastq  ER2_GCCAAT_L002_R2_001.fastq
ER3_CAGATC_L002_R1_001.fastq  ER3_CAGATC_L002_R2_001.fastq

Mo1_CGATGT_L002_R1_001.fastq  Mo1_CGATGT_L002_R2_001.fastq
Mo3_CTTGTA_L002_R1_001.fastq  Mo3_CTTGTA_L002_R2_001.fastq 

NC1_ATGTCA_L002_R1_001.fastq  NC1_ATGTCA_L002_R2_001.fastq
NC2_CCGTCC_L002_R1_001.fastq  NC2_CCGTCC_L002_R2_001.fastq
NC3_GTCCGC_L002_R1_001.fastq  NC3_GTCCGC_L002_R2_001.fastq
 
SK1_AGTCAA_L002_R1_001.fastq  SK1_AGTCAA_L002_R2_001.fastq
SK2_TGACCA_L002_R1_001.fastq  SK2_TGACCA_L002_R2_001.fastq
SK3_AGTTCC_L002_R1_001.fastq  SK3_AGTTCC_L002_R2_001.fastq
