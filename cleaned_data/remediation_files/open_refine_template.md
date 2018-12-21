# Open Refine Template for Phoenix


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["identifier"].value}}</identifier>
<identifier type="pid">{{cells["PID"].value}}</identifier>
<titleInfo supplied="yes"><title>{{cells['title'].value}}</title></titleInfo>
<abstract>Phoenix is a student-led literary publication, showcasing the creative output of UT's diverse student population, including photography, illustration, poetry, fiction, and non-fiction.</abstract>
<note>Publications by students.</note>
<name type="corporate" valueURI="http://id.loc.gov/authorities/names/n80003887">
<namePart>University of Tennessee (Knoxville campus)</namePart>
<role>
<roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre">Creator</roleTerm>
</role>
</name>
{{if(isBlank(cells['editor'].value), '', '<name' + if(isBlank(cells['editor_URI'].value), '', ' authority="naf" valueURI="' + cells['editor_URI'].value + '"') + '><namePart>' + cells['editor'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/edt">Editor</roleTerm></role></name>')}}
{{if(isBlank(cells['artist'].value), '', '<name><namePart>' + cells['artist'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/art">Artist</roleTerm></role></name>')}}
{{if(isBlank(cells['artist_editor'].value), '', '<name><namePart>' + cells['artist_editor'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/edt">Editor</roleTerm><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/art">Artist</roleTerm></role></name>')}}
<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300215389"></form>magazines (periodicals)</physicalDescription>
<originInfo><dateIssued>{{cells['date_text'].value}}</dateIssued><dateIssued encoding="edtf">{{cells['date_edtf'].value}}</dateIssued><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm></place></originInfo>
<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh85028351"><topic>College student newspapers and periodicals</topic></subject>


<typeOfResource>text</typeOfResource>
<typeOfResource>still image</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Mugwump</title></titleInfo></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<classification authority="lcc">LH1.T2 P3</classification>
<language><languageTerm type="text" authority="iso639-2b">English</languageTerm></language>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource><languageOfCataloging><languageTerm type="text" authority="iso639-2b">English</languageTerm></languageOfCataloging><recordOrigin>
Created and edited in general conformance to MODS Guidelines (Version 3.5).
</recordOrigin></recordInfo>
<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/InC/1.0/">In Copyright</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```