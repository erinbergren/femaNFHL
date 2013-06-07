femaNFHL
====================

This page has information on flood zone/flood risk designation data from Federal Emergency Managment Agency (FEMA)'s National Flood Hazard Layer Database (NFHL). If you are interested in getting FEMA's GIS maps for an entire State or for the entire US, then you might find the below information useful.

FEMA provides a variety of flood risk maps, most popular ones being the flood insurance rate maps (FIRMs). The [product catalog](https://msc.fema.gov/webapp/wcs/stores/servlet/StoreCatalogDisplay?storeId=10001&catalogId=10001&langId=-1&userType=G) from FEMA lists these products. More information is also available from FEMA's [map service center](https://msc.fema.gov/).

After scanning through FEMA's [product catalog](https://msc.fema.gov/webapp/wcs/stores/servlet/StoreCatalogDisplay?storeId=10001&catalogId=10001&langId=-1&userType=G) and this [FEMA document](http://www.fema.gov/library/viewRecord.do?id=3474) and the below websites, the NFHL dataset is your best bet if you do not want to spend money. If you have money to spend and/or if you want information specific to a neighborhood or community, then use the other products in the catalog.
* A good description of what NFHL is from the State of Massachussetts' [GIS dept](http://www.mass.gov/anf/research-and-tech/it-serv-and-support/application-serv/office-of-geographic-information-massgis/datalayers/nfhl.html)
* PDF from a FEMA [workshop at Michael Baker Corp](http://www.bakeraecom.com/wp-content/upLoads/2010/03/DFIRM101_Workshop1.pdf), 3/2010
* PDF from a [seminar by FEMA at Montana DNRC?](http://www.dnrc.mt.gov/wrd/water_op/floodplain/2009_seminar/gis_basics_for_floodplain_mgmt.pdf), 4/2009


### Where to get the NFHL GIS data and what to get

You can get the [NFHL database](https://msc.fema.gov/webapp/wcs/stores/servlet/CategoryDisplay?catalogId=10001&storeId=10001&categoryId=12011&langId=-1&userType=G&type=12) by state. 


Attributes of the NFHL Shapefiles
--------------------

The FEMA [website](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=2&ved=0CDgQFjAB&url=http%3A%2F%2Fwww.fema.gov%2Flibrary%2Ffile%3Ftype%3DpublishedFile%26file%3Dnfhl_gisdata_june2010.pdf%26fileid%3D33402f00-839e-11df-af73-001cc4568fb6&ei=2zySUbvBD-SdiQK8zYHIBQ&usg=AFQjCNHKLZdOTW4qNJmbR4tvKan5F-5Wig&sig2=Y5HDjNg8bJsdd2GhovOCPQ&bvm=bv.46471029,d.cGE), describes the fields in the shapefiles, but is not complete. The shapefile "S_FLD_HAZ_AR.shp" could have the following fields (or more?):

* OBJECT_ID
* DFIRM_ID
* FLD_AR_ID
* FLD_ZONE: Flood zone designation
* FLOODWAY: Designation of the area as a floodway
* SFHA_TF: Identification of the zone as being an SFHA
* STATIC_BFE: Static BFE
* V_DATUM 
* DEPTH: Depth value for certain zones
* LEN_UNIT
* VELOCITY: Velocity measurements for alluvial fans in certain Zone AO areas 
* VEL_UNIT
* If the FLD_ZONE field identifies the area as being Zone AR, information about the zone to which the area would revert - 
  * AR_REVERT
  * BFE_REVERT
  * DEP_REVERT
  * LEN_UNIT
  * V_DATUM
* SOURCE_CIT
* HYDRO_ID
* CST_MDL_ID

The most relevant variable in the above list is "FLD_ZONE" which could take one of five types of [flood zone designations](https://msc.fema.gov/webapp/wcs/stores/servlet/info?storeId=10001&catalogId=10001&langId=-1&content=floodZones&title=FEMA%2520Flood%2520Zone%2520Designations):
* High Risk Areas (non-Coastal): "A", "AE", "A1" to "A30", "AH", "AO", "AR", "A99" 
* High Risk Coastal Areas: "V", "VE", "V1" to "V30"
* Moderate Risk: "B", "X (shaded)"
* Low Risk: "C", "X (unshaded)"
* Unknown Risk: "D"


Other useful websites:
--------------------
* [Flood map viewer from FEMA](https://hazards.fema.gov/wps/portal/mapviewer)
* [Hazard Map Viewer from FEMA](https://hazards.fema.gov/femaportal/wps/portal/mmvmapviewer)
* [FEMA 100-yr Flood zones map for the US](http://www.arcgis.com/home/webmap/viewer.html?webmap=2e38c1d9c2494fcfbe21384f3ddfecb4)
* [Web Map Service for the NFHL](https://hazards.fema.gov/femaportal/wps/portal/NFHLWMS)
* [Google Earth KMZ files](https://hazards.fema.gov/femaportal/wps/portal/NFHLWMSkmzdownload)

