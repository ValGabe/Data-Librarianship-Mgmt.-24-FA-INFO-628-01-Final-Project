README

Import the cleaned individual datasets into QGIS as separate map layers:
Layer > Add Layer > Add Delimited Text Layer
The X and Y fields should correspond to Latitude and Longitude, 

All layers should be placed above the world map layer.

To generate a world map: 
Go to the coordinate field and type 'world' that will generate a worldwide vector layer

The code in the Field Calculator will check the gender column and assign the corresponding count value if the gender matches, otherwise, it will assign a value of 0.

Code for Gender-Specific Fields
1. Female Count
if("gender" = 'female', "count", 0)

2. Female (Transwoman) Count
if("gender" = 'female (transwoman)', "count", 0)

3. Gender Non-Conforming Count
if("gender" = 'gender non-conforming', "count", 0)

4. Male Count
if("gender" = 'male', "count", 0)

5. Non-Binary Count
if("gender" = 'non-binary', "count", 0)

6. Blank Count
if("gender" = '', "count", 0)

How to Create Gender-Specific Count Fields:
Open the Attribute Table for your centroid layer.

Open the Field Calculator (the abacus icon at the top of the attribute table).

In the Field Calculator dialog:
Field Name: Enter the name for the field (e.g., Female_Count, Male_Count, etc.).

Output Field Type: Select Integer.

Expression: Paste the relevant code above for each gender.

Click OK to create the new field.

Repeat the above process for each gender field (Female, Male, Transwoman, etc.).
This will create a set of fields that represent the count of each gender at the corresponding centroids.

To create heatmaps, right click on each layer > properties > symbology > and change the topmost field into graduated 
