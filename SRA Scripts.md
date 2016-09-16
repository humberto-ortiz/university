SRA SCRIPTS:

MODEL:

	      /  1 cave   \
ASTYANAX:-			   - 2 Individuals
	      \ 1 surface /

	      	  /  2 cave   \
Sinocheilus: -			   - 4 Individuals
			  \ 2 surface /

REFERENCE SCRIPT:

#!/bin/sh
#SBATCH --time 2:00:00
#SBATCH -p debug -n 16
#SBATCH --job-name=download
#SBATCH --output=download.out
#SBATCH --error=download.err
#SBATCH --mail-type=ALL
#SBATCH --mail-user=andrewwt@gwu.edu


module load sra

cd /home/andrewwt

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRR2001231
mv /home/andrewwt/SRR2001231_1.fastq /home/andrewwt/kmar_postdiapause.fq

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRR2001227
mv /home/andrewwt/SRR2001227_1.fastq /home/andrewwt/Kmar_diapauserep3.fq

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRR2001221	
mv /home/andrewwt/SRR2001221_1.fastq /home/andrewwt/Kmar_diapauserep2.fq

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRR2001218	
mv /home/andrewwt/SRR2001218_1.fastq /home/andrewwt/Kmar_diapauserep1.fq

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRR1999414
mv /home/andrewwt/SRR1999414_1.fastq /home/andrewwt/Kmar_prediapause.fq

SCRIPT:

#!/bin/sh
#SBATCH --time 2:00:00
#SBATCH -p debug -n 16
#SBATCH --job-name=download
#SBATCH --output=download.out
#SBATCH --error=download.err
#SBATCH --mail-type=ALL
#SBATCH --mail-user=david.ortiz11@upr.edu

cd /storage/home/dortiz/

// ASTYANAX CAVEFISH PACHON, SRX212201

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRX212201 mv /storage/home/dortiz/SRX212201.fastq /storage/home/dortiz/AST01_SRX212201.fq

// ASTYANAX SURFACE FISH, SRX212200

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRX212200 mv /storage/home/dortiz/SRX212200.fastq /storage/home/dortiz/AST02_SRX212200.fq

// SURFACE FISH, SRR788094

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRR788094 mv /storage/home/dortiz/SRR788094.fastq /storage/home/dortiz/SINSF01_SRR788094.fq

// CAVEFISH,SRR788095

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRR788095 mv /storage/home/dortiz/SRR788095.fastq /storage/home/dortiz/SINCF01_SRR788095.fq

// SURFACE FISH, SRR788096

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRR788096 mv /storage/home/dortiz/SRR788096.fastq /storage/home/dortiz/SINSF01_SRR788096.fq

// CAVEFISH, SRR788097

fastq-dump --defline-seq '@$sn[_$rn]/$ri' --split-files SRR788097 mv /storage/home/dortiz/SRR788097.fastq /storage/home/dortiz/SINCF02_SRR788097.fq
