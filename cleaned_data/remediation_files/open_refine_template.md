# OpenRefine Template for W. O. Garner Collection (Remediation)

---

## Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```

## Row Template

```
<mods>
<identifier type="pid">{{cells['PID'].value}}</identifier>
<identifier type="original ID">{{cells['OriginalID'].value}}</identifier>
<identifier type="document ID">{{cells['identifier_docID'].value}}</identifier>
{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>')}}
{{if(isBlank(cells['alternate_title'].value), '', '<titleInfo type="alternative"><title>' + cells['alternate_title'].value + '</title></titleInfo>')}}
{{if(isBlank(cells['abstract'].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells['creator'].value), '', '<name' + if(isBlank(cells['creator_URI'].value), '', ' authority="naf" valueURI="' + cells['creator_URI'].value + '"') + '><namePart>' + cells['creator'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['role_URI'].value + '">' + cells['role'].value + '</roleTerm></role></name>')}}
{{'<originInfo>' + if(isBlank(cells['dateCreated_year'].value), '', '<dateCreated>' + cells['dateCreated_year'].value + '</dateCreated><dateCreated encoding="edtf" keyDate="yes">' + cells['dateCreated_year'].value + '</dateCreated>') + if(isBlank(cells['dateCreated_exact'].value), '', '<dateCreated>' + cells['dateCreated_exact'].value + '</dateCreated><dateCreated encoding="edtf" keyDate="yes">' + cells['dateCreated_exact_edtf'].value + '</dateCreated>') + if(isBlank(cells['dateCreated'].value), '', '<dateCreated>' + cells['dateCreated'].value + '</dateCreated><dateCreated encoding="edtf" point="start" keyDate="yes">' + cells['dateCreated_edtf_start'].value + '</dateCreated><dateCreated encoding="edtf" point="end">' + cells['dateCreated_edtf_end'].value + '</dateCreated>') + '</originInfo>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form>
<extent>{{cells['extent'].value}}</extent><internetMediaType>{{cells['internetMediaType'].value}}</internetMediaType></physicalDescription>
{{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}}
<note displayLabel="Intermediate Provider">University of Tennessee, Knoxville. Libraries</note>
{{if(isBlank(cells['subject_topic'].value), '', '<subject authority="' + cells['subject_topic_auth'].value + '" valueURI="' + cells['subject_topic_URI'].value + '"><topic>' + cells['subject_topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic2'].value), '', '<subject authority="' + cells['subject_topic2_auth'].value + '" valueURI="' + cells['subject_topic2_URI'].value + '"><topic>' + cells['subject_topic2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic3'].value), '', '<subject authority="' + cells['subject_topic3_auth'].value + '" valueURI="' + cells['subject_topic3_URI'].value + '"><topic>' + cells['subject_topic3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic4'].value), '', '<subject authority="' + cells['subject_topic4_auth'].value + '" valueURI="' + cells['subject_topic4_URI'].value + '"><topic>' + cells['subject_topic4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic5'].value), '', '<subject authority="' + cells['subject_topic5_auth'].value + '" valueURI="' + cells['subject_topic5_URI'].value + '"><topic>' + cells['subject_topic5'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic6'].value), '', '<subject authority="' + cells['subject_topic6_auth'].value + '" valueURI="' + cells['subject_topic6_URI'].value + '"><topic>' + cells['subject_topic6'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic7'].value), '', '<subject authority="' + cells['subject_topic7_auth'].value + '" valueURI="' + cells['subject_topic7_URI'].value + '"><topic>' + cells['subject_topic7'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic8'].value), '', '<subject authority="' + cells['subject_topic8_auth'].value + '" valueURI="' + cells['subject_topic8_URI'].value + '"><topic>' + cells['subject_topic8'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic9'].value), '', '<subject authority="' + cells['subject_topic9_auth'].value + '" valueURI="' + cells['subject_topic9_URI'].value + '"><topic>' + cells['subject_topic9'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic10'].value), '', '<subject authority="' + cells['subject_topic10_auth'].value + '" valueURI="' + cells['subject_topic10_URI'].value + '"><topic>' + cells['subject_topic10'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic11'].value), '', '<subject authority="' + cells['subject_topic11_auth'].value + '" valueURI="' + cells['subject_topic11_URI'].value + '"><topic>' + cells['subject_topic11'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic12'].value), '', '<subject authority="' + cells['subject_topic12_auth'].value + '" valueURI="' + cells['subject_topic12_URI'].value + '"><topic>' + cells['subject_topic12'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic13'].value), '', '<subject authority="' + cells['subject_topic13_auth'].value + '" valueURI="' + cells['subject_topic13_URI'].value + '"><topic>' + cells['subject_topic13'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic14'].value), '', '<subject authority="' + cells['subject_topic14_auth'].value + '" valueURI="' + cells['subject_topic14_URI'].value + '"><topic>' + cells['subject_topic14'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic15'].value), '', '<subject authority="' + cells['subject_topic15_auth'].value + '" valueURI="' + cells['subject_topic15_URI'].value + '"><topic>' + cells['subject_topic15'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic16'].value), '', '<subject authority="' + cells['subject_topic16_auth'].value + '" valueURI="' + cells['subject_topic16_URI'].value + '"><topic>' + cells['subject_topic16'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic17'].value), '', '<subject authority="' + cells['subject_topic17_auth'].value + '" valueURI="' + cells['subject_topic17_URI'].value + '"><topic>' + cells['subject_topic17'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic18'].value), '', '<subject authority="' + cells['subject_topic18_auth'].value + '" valueURI="' + cells['subject_topic18_URI'].value + '"><topic>' + cells['subject_topic18'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic19'].value), '', '<subject authority="' + cells['subject_topic19_auth'].value + '" valueURI="' + cells['subject_topic19_URI'].value + '"><topic>' + cells['subject_topic19'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic20'].value), '', '<subject authority="' + cells['subject_topic20_auth'].value + '" valueURI="' + cells['subject_topic20_URI'].value + '"><topic>' + cells['subject_topic20'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic21'].value), '', '<subject authority="' + cells['subject_topic21_auth'].value + '" valueURI="' + cells['subject_topic21_URI'].value + '"><topic>' + cells['subject_topic21'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic22'].value), '', '<subject authority="' + cells['subject_topic22_auth'].value + '" valueURI="' + cells['subject_topic22_URI'].value + '"><topic>' + cells['subject_topic22'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic23'].value), '', '<subject authority="' + cells['subject_topic23_auth'].value + '" valueURI="' + cells['subject_topic23_URI'].value + '"><topic>' + cells['subject_topic23'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic24'].value), '', '<subject authority="' + cells['subject_topic24_auth'].value + '" valueURI="' + cells['subject_topic24_URI'].value + '"><topic>' + cells['subject_topic24'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic25'].value), '', '<subject authority="' + cells['subject_topic25_auth'].value + '" valueURI="' + cells['subject_topic25_URI'].value + '"><topic>' + cells['subject_topic25'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject' + if(isBlank(cells['subject_name_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name_URI'].value + '"') + '><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name2'].value), '', '<subject' + if(isBlank(cells['subject_name2_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name2_URI'].value + '"') + '><name><namePart>' + cells['subject_name2'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name3'].value), '', '<subject><name><namePart>' + cells['subject_name3'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_geo'].value), '', '<subject authority="' + cells['subject_geo_auth'].value + '" valueURI="' + cells['subject_geo_URI'].value + '"><geographic>' + cells['subject_geo'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geo2'].value), '', '<subject authority="' + cells['subject_geo2_auth'].value + '" valueURI="' + cells['subject_geo2_URI'].value + '"><geographic>' + cells['subject_geo2'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geo3'].value), '', '<subject authority="' + cells['subject_geo3_auth'].value + '" valueURI="' + cells['subject_geo3_URI'].value + '"><geographic>' + cells['subject_geo3'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geo4'].value), '', '<subject authority="' + cells['subject_geo4_auth'].value + '" valueURI="' + cells['subject_geo4_URI'].value + '"><geographic>' + cells['subject_geo4'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geo5'].value), '', '<subject authority="' + cells['subject_geo5_auth'].value + '" valueURI="' + cells['subject_geo5_URI'].value + '"><geographic>' + cells['subject_geo5'].value + '</geographic></subject>')}}
<language><languageTerm type="text" authority="iso639-2b">{{cells['language'].value}}</languageTerm></language>
<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>W. O. Garner Photograph Collection</title></titleInfo></relatedItem>
{{if(isBlank(cells['relatedItem_title'].value), '', '<relatedItem type="otherFormat"><titleInfo><title>' + cells['relatedItem_title'].value + '</title><titleInfo><publisher>' + cells['relatedItem_publisher'].value + '</publisher><dateIssued>' + cells['relatedItem_dateIssued'].value + '</dateIssued><note>' + cells['relatedItem_pages'].value + '</note></relateItem>')}}
<location><physicalLocation>Blount County Public Library</physicalLocation></location>
<recordInfo><recordContentSource>Blount County Public Library</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>
```

## Row Separator

**LEAVE BLANK**

## Suffix

```
</modsCollection>
```