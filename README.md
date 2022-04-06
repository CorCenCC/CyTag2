# CyTag2

Fersiwn newydd tagiwr rhan ymadrodd y brosiect CorCenCC.

New version of the CorCenCC project's part-of-speech tagger.

<details><summary>Cyfarwyddiadau Cymraeg</summary>
<p>

## Cyn Cychwyn

Pan rhedwch y cod am y tro cyntaf, mae'n *rhaid* i chi ddewis yr opsiwn i ail-adeiladu'r ffeiliau lecsicon. 

Defnyddiwch y gorchymyn:

```
python app.py
```

heb unrhyw fflagiau. Fydd y rhyngwyneb llinell orchymyn yn eich promptio i osod dewisiadau. Atebwch "I" i'r cwestiwn "Hoffech (ail-)adeiladu'r lecsica?"

Os na wnewch chi hyn am y tro cyntaf, fe fydd y cod yn methu.


## Ffeiliau mewnbwn

Mae CorCenCC yn disgwyl ffeiliau .txt. Rhowch eich ffeiliau mewnbwn yn y ffolder `txt`, sydd o fewn ffolder y brosiect CyTag2.

## Dewisiadau

Os alwch y cod heb fflagiau, fe'ch gofynnir i gadarnhau y dewisiadau canlynol:

Iaith y rhyngwyneb
: Cewch ddewis cael negeseuon allbwn yn y Gymraeg neu'r Saesneg.

Enw'r ffolder allbwn
: Dewiswch enw i'r ffolder fydd yn dal eich allbwn o fewn y ffolder cyffredinol `allbwn` (neu `output` os Saesneg ydy iaith y rhyngwyneb).
**Fe fydd CyTag2 yn trosysgrifo allbwn blaenorol os dewiswch enw ffolder sydd eisioes yn bodoli.** Ni chewch rhybydd os dewiswch enw sydd eisioes yn bodoli. Oherwydd hyn, fe'ch cynghorir i symud eich ffeiliau allan o ffolder allbwn CyTag unwaith y byddwch yn hapus gyda canlyniadau'r tagiwr.

(Ail-)adeiladu'r lecsica
: Mae gan CyTag2 ffeiliau lecsicon, sy'n rhestru geiriau a'u rhannau ymadrodd. Rhaid adeiliadu geiriaduron Python gyda'r data o'r lecsica. Gall hyn cymryd tipyn o amser, yn enwedig pan yn adeiladu rhestri enwau priod. Oherwydd hyn, mae'n well peidio ail-adeiladu'r lecsica oni bai'ch bod chi wedi gwneud unrhyw newidiadau iddyn nhw. (Yr eithriad ydy'r tro gyntaf i chi ddefnyddio CyTag: gweler uchod am gyfarwyddiadau.)

(Ail-)osod y rhestr geiriau anhysbus
: Mae'r rhestr geiriau anhysbys yn cadw cofnod o eiriau nad oedd CyTag yn medru eu hadnabod. Os dewiswch ail-osod y rhestr, caiff canlyniadau blaenorol eu dileu. Os dewiswch beidio ag ail-osod, yna ysgrifennir canlyniadau newydd ar ddiwedd y ffeil, ar ôl y canlyniadau sydd eisioes yn bod.


### Fflagiau llinell gorchymun

Mae CyTag2 yn cynnig nifer o fflagiau y gellir ei defnyddio o'r llinell gorchymun.

| Fflag | Disgrifiad |
| ----------- | ----------- |
| `-c` | Rhedeg y cod gyda'r rhagosodiadau canlynol: Cymraeg fel iaith y rhyngwyneb; ffolder allbwn `cytag`; ail-osod y rhestr geiriau anhysbus; peidio ail-adeiladu'r lecsica (oni bai bo'r fflag `-l` hefyd yn cael ei defnyddio) |
| `-l` | Ail-adeiladu'r lecsica Cymraeg a Saesneg, ond nid y rhestri enwau priod. (Cyflymach o lawer na dewis ail-adeiladu'r holl lecsica.)|
| `-b` | Enwi blaenddodiad er mwyn hidlo ffeiliau mewnbwn. Fe fydd CyTag2 yn prosesu dim ond y ffeiliau a'r mewnbwn a enwyd. E.e. enwch `newydd_` er mwyn prosesu'r ffeil `newydd_data.txt` ac anwybyddu'r ffeil `data.txt`.|
| `-p` | Fflag er mwyn rhag-brosesu data CorCenCC. Dylid defnyddio'r fflag yn unig pan yn prosesu data CorCenCC. |

## VISL-CG3

Mae CyTag2 yn defnyddio ffurfiolaeth gramadeg cyfyngiadau er mwyn tagio testunau. Fe fydd angen i chi osod cod y brosiect VISL-CG3 ar eich cyfrifiadur cyn rhedeg CyTag2 am y tro cyntaf.

Gellir lawrlwytho cod VISL-CG3 drwy ymweld â https://github.com/GrammarSoft/cg3
</p>
</details>

<details><summary>English Instructions</summary>
<p>

## Before Starting

When you run the code for the first time, you *must* select the option to build the lexicon files.

Use the command

```
python app.py
```
with no flags. The command-line interface will prompt you to set preferences. Answer "Y" to the question "Do you want to (re)build the lexica?"

If you don't do this, the code will fail.

## Input files

CorCenCC expects .txt format files. Place your input file(s) into the `txt` folder, which is in the CyTag2 project folder.

## Options

If you use no flags, you will be asked to confirm the following options:

Interface language
: Choose Welsh or English as the language for messages and outputs.

Output folder name
: Choose a name for the subfolder which will hold your results in the general `output` folder (or `allbwn` folder, if the interface language is set to Welsh).
**CyTag2 will overwrite previous outputs if you choose a folder name that already exists.** You will not be warned if you choose a pre-existing folder name. You are therefore advised to move your files out of the CyTag output folder once you are satisfied with a set of results from the tagger.

(Re-)build the lexica
: CyTag uses lexicon files, which list words and their part of speech. Python dictionaries are constructed from the lexicon data. This can be time-consuming, especially when building the lists of proper nouns. As a result, it's best not to rebuild the lexica unless you have made any changes to the files. (The exception is the first time you run the code; see above for instructions.)

(Re-)set the list of unknown words
: The unknown word list keeps a record of words which CyTag2 was unable to recognise. If you choose to reset the list, CyTag will overwrite any previous results. Otherwise, new results will be appended to the end of the existing list.

### Command-line flags
CyTag2 offers a number of command-line flags:

| Flag | Description |
| ----------- | ----------- |
| `-c` | Run the code with the following defaults: Welsh as the interface language; `cytag` output folder name; reset the list of unknown words; don't refresh the lexica (unless the `-l` flag is also used) |
| `-l` | Rebuild the Welsh and English lexica, but not the lists of proper nouns. (Much faster than rebuilding all of the lexica.)|
| `-b` | Name a prefix to filter input files. Only files with the specified prefix will be processed. E.g. specify `new_` to process the file `new_data.txt` and ignore the file `data.txt`. |
| `-p` | A flag to preprocess CorCenCC data. Should only be used when processing CorCenCC project data. |


## VISL-CG3

CyTag2 uses the constraint grammar formalism to tag texts. You will need to install the VISL-CG3 project's code on your computer before running CyTag2 for the first time.

The VISL-CG3 code can be cloned from https://github.com/GrammarSoft/cg3
</p>
</details>