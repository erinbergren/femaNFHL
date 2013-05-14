femaNFHL
====================

Repository containing overview info on Federal Emergency Managment Agency (FEMA)'s National Flood Hazard Layer Database (NFHL).

Flood Maps from FEMA
--------------------

FEMA provides a variety of flood risk maps. Most popular among them are the flood insurance rate maps (FIRMs). The [product catalog](https://msc.fema.gov/webapp/wcs/stores/servlet/StoreCatalogDisplay?storeId=10001&catalogId=10001&langId=-1&userType=G) from FEMA lists these products, but it is not very clear from this page as to which one is to be used,  their availability, spatial extent, price, etc.

Following is a list of useful and informative websites:
* A good description of what NHFL is from the State of Massachussetts' [GIS dept](http://www.mass.gov/anf/research-and-tech/it-serv-and-support/application-serv/office-of-geographic-information-massgis/datalayers/nfhl.html)
* PDF from a FEMA [workshop at Michael Baker Corp](http://www.bakeraecom.com/wp-content/upLoads/2010/03/DFIRM101_Workshop1.pdf), 3/2010
* PDF from a [seminar by FEMA at Montana DNRC?](http://www.dnrc.mt.gov/wrd/water_op/floodplain/2009_seminar/gis_basics_for_floodplain_mgmt.pdf), 4/2009

Othe related and useful websites:
* [Flood map viewer from FEMA](https://hazards.fema.gov/wps/portal/mapviewer)
* [Hazard Map Viewer from FEMA](https://hazards.fema.gov/femaportal/wps/portal/mmvmapviewer)
* [FEMA 100-yr Flood zones map for the US](http://www.arcgis.com/home/webmap/viewer.html?webmap=2e38c1d9c2494fcfbe21384f3ddfecb4)


Where to get the data and what to get
--------------------


### Attributes of the NFHL Shapefiles

Edited text from the FEMA [website](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=2&ved=0CDgQFjAB&url=http%3A%2F%2Fwww.fema.gov%2Flibrary%2Ffile%3Ftype%3DpublishedFile%26file%3Dnfhl_gisdata_june2010.pdf%26fileid%3D33402f00-839e-11df-af73-001cc4568fb6&ei=2zySUbvBD-SdiQK8zYHIBQ&usg=AFQjCNHKLZdOTW4qNJmbR4tvKan5F-5Wig&sig2=Y5HDjNg8bJsdd2GhovOCPQ&bvm=bv.46471029,d.cGE):

Five information themes are of common interest to users:

1. flood hazard zones
2. cross sections
3. communities
4. FIRMs, and 
5. LOMRs

**Flood hazard zones**: The table S_Fld_Haz_Ar contains information about flood hazards. The associated spatial data are polygons. Standard fields record the:
* Flood zone designation (field FLD_ZONE).
*  Identification of the zone as being an SFHA (field SFHA_TF).
* Designation of the area as a floodway (field FLOODWAY).
* Static BFE (fields STATIC_BFE, LEN_UNIT, and V_DATUM) for certain zones.
* Depth value for certain zones (fields DEPTH and LEN_UNIT).
* Velocity measurements for alluvial fans in certain Zone AO areas (fields VELOCITY and
VEL_UNIT).
* If the FLD_ZONE field identifies the area as being Zone AR, information about the zone to which the area would revert (fields AR_REVERT, BFE_REVERT, DEP_REVERT, LEN_UNIT, and V_DATUM).

**Cross sections**: When used with the Flood Insurance Study (FIS) for the community, cross sections are the basis for calculating a BFE. The table S_XS contains information about cross sections. The associated spatial data are lines. Standard fields record the:
* Regulatory water-surface elevation for the 1-percent-annualchance flood event (fields WSEL_REG, LEN_ UNIT, and V_DATUM).
* Measurement along the stream from a specified point to the cross section (field STREAM_STN).
* Letter or number assigned to the cross section on the FIRM and in the FIS report (field XS_LTR).
* Name of the primary water feature spanned by the cross section (field WTR_NM).

**Communities**: The table S_Pol_Ar contains information about political areas, including political jurisdictions and other areas such as forests, parks, and military lands. The associated spatial data are polygons. Standard fields record the:
* Primary and secondary names (fields POL_NAME1 and POL_NAME2).
* State and county Federal Information Processing Standard (FIPS) code (fields ST_FIPS and CO_FIPS respectively).
* Community Number and Community Identification Number (CID) (fields COMM_NO and CID respectively).
* Database link (field COM_NFO_ID) to a look up table (table L_Comm_Info) that has additional information about the community.

**FIRM panel layouts**: The table S_FIRM_Pan contains information about the FIRM panels. The associated spatial data are polygons. Standard fields record the:
* Panel number (stored in its entirety in field FIRM_PAN, and by its components in fields ST_FIPS, PCOMM, PANEL, and SUFFIX).
* Effective date (field EFF_DATE).
* Map scale (field SCALE).
* Print status and project type (field PANEL_TYP) and, if not printed, the reason (field PNP_REASON).
* Corner coordinates for the FIRM panel (fields NW_LAT, NW_LONG, SE_LAT, and SE_LONG).

**LOMRs**: The table S_LOMR contains information about the area affected by LOMRs. The associated spatial data are polygons. Standard fields record the:
* Case number (field CASE_NO).
* Effective date (field EFF_DATE).
* Map scale (field SCALE).
* Status (field STATUS).



