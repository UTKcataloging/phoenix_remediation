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
<titleInfo supplied="yes"><title>{{cells['title'].value}}</title>{{if(isBlank(cells['volume_number'].value), '', '<partNumber>' + cells['volume_number'].value + '</partNumber>')}}</titleInfo>
{{if(isBlank(cells['note'].value), '', '<abstract>' + cells['note'].value + '</abstract>')}}
<abstract>Phoenix is a student-led literary publication, showcasing the creative output of UT's diverse student population, including photography, illustration, poetry, fiction, non-fiction, and interviews.</abstract>
<name type="corporate" authority="naf" valueURI="{{cells['creator_URI'].value}}"><namePart>{{cells['creator'].value}}</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre">Creator</roleTerm></role></name>
{{if(isBlank(cells['author'].value), '', '<name' + if(isBlank(cells['author_URI'].value), '', ' authority="naf" valueURI="' + cells['author_URI'].value + '"') + '><namePart>' + cells['author'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300215389">magazines (periodicals)</form></physicalDescription>
<originInfo><dateIssued>{{cells['date_year'].value}}</dateIssued><dateIssued encoding="edtf">{{cells['date_edtf'].value}}</dateIssued><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm></place></originInfo>
<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh85028351"><topic>College student newspapers and periodicals</topic></subject>
{{if(isBlank(cells['subject7'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject7_URI'].value + '"><topic>' + cells['subject7'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject8'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject8_URI'].value + '"><topic>' + cells['subject8'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject5'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject5_URI'].value + '"><topic>' + cells['subject5'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject6'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject6_URI'].value + '"><topic>' + cells['subject6'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_geo'].value), '', '<subject authority="naf" valueURI="' + cells['subject_geo_URI'].value + '"><geographic>' + cells['subject_geo'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject' + if(isBlank(cells['subject_name_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name_URI'].value + '"') + '><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject2_name'].value), '', '<subject' + if(isBlank(cells['subject2_name_URI'].value), '', ' authority="naf" valueURI="' + cells['subject2_name_URI'].value + '"') + '><name><namePart>' + cells['subject2_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject3_name'].value), '', '<subject' + if(isBlank(cells['subject3_name_URI'].value), '', ' authority="naf" valueURI="' + cells['subject3_name_URI'].value + '"') + '><name><namePart>' + cells['subject3_name'].value + '</namePart></name></subject>')}}
<typeOfResource>text</typeOfResource>
<typeOfResource>still image</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Phoenix</title></titleInfo></relatedItem>
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