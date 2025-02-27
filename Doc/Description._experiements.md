# Description of the Experiments 

The Doc `Planning_EXP_plume.xlsx` is the original file where all the information about the experiments has been written. 

This file contains raw information (some of which such as stratification must be obtained from measurements) and is difficult to read.

In order to facilitate the sharing of this information, a database has been created and made available [here](https://mirror-mustard-600.notion.site/af450998205d4596a9c1e90e7781de3e?v=4a520f079561431db26593f76c7b3f04&pvs=4)

If you have any questions about this database or about the experiments feel free to send a mail to max.coppin@univ-grenoble-alpes.fr 



## Experiement's description  

### Two Configuration
- KP 

- RB 


## Database architecture

The database was built using Notion software (https://www.notion.so). It is organised as follows: 
- Lignes: the different experiments carried out*. 
- Columns: the different characteristics of the experiments (detailed below)

note: Several experiments may have been carried out one after the other (for a single start of the heating system). For organisational reasons, two experiments are separated if the same measuring instrument is used twice. 
Volume acquisition and PIV acquisition of the vertical slice are never simultaneous.


Several ‘views’ are available to filter the columns. Simply click on these below the title.

### Views: 
- all: displays all experiments 
- Description: Gathers all the information on the physics of experiments. Preferred view for reproducing experiments numerically or for data analysis.
- UVMAT- PCO: Follow up the processing of PIV images acquired with PCO cameras (processing on [UVMAT software](https://servforge.legi.grenoble-inp.fr/projects/soft-uvmat)))
- UVMAT- JAI: Same but for the JAI camera
- Stress : filter only the experiment with stress (KP and KP + heating)
- Rotation : idem for rotation 
- Startification : Idem 

### Caracteristiques : 

- **Type** : Type of configuration
    - KP for Kato-Phillips  (Bottom stress/Spin-up experiment)
    - RB for Rayeigh-Benard (all experiments in this section are performed with the heating plate ON **exept** EXP22_3)
    
- **Nature** : Classification/specification of the experiement
    - *Rb*: (Only heating)
    - *Rotation*: means the experiment was performed with an initial rotation (The rotation is precised in the **f** column)
    - *Stratification*: means the experiment was performed with by default a thermal stratification (The rotation is precised in the **Stratif N** column)
    - *Strat +Rotation*:
    - *Stratification salt*: -> Haline stable stratification 
    - *Heat off*: The heating system was turned off at the begining of the experiment
    - *Stress*: A rotation )or acceleration of the rotation if already rotating) is applied to the plateform at the very begining og the experiment 
    - *Colorant*: A Dye (Rhodamine-G) is injected near the plate (in the heavyer layer of the water column 
    - *LIF*: A uniform concentration ($C=10\times )Dye (Rhodamine-B) 
    - *1meter*: The height of the water column was $1$m (all the other had $0.5$ m )
    
- **Observed Field**: 
    - *Vertical*: The data concerns the vertical plane (width $=30$cm; height $=26$cm)/(width $=50$cm; height $=45$cm for The experiment with 1m ) perpendicular to the radius (at $4.5$ m )
    - *Horizontal*: The horizontal plan is a square (width $=3$m; lenght $=4$m) at $10$ cm above the heat plate  
    - *Volume 3D*: Data is aaqcuires on the horizontal plane on several height (in range of approx $2$cm - $40$ cm) giving a 3D volume
- **Frequence acuisition PIV** : 
    - Frequency between two images.
- ** Heat time**: total time where the heating system were ON (long series are recorded with vertical temperature profilers and fixed thermistances)
    - Note this given time is approximate but can be found precisely on the *LABVIEW* data 
- ** Heating Time at PIV aquisition**: Time of heating before the start of PIV acquisition
    - The triger of the PIV is recorded in `TRIG_CAM` variable of the *LABVIEW* data. This is the data which is use to synchronize the temperature and velocity data (needed for turbulent heat fluxes)
- ** PIV acquisition Time**: Duration of the PIV acquition 
    - Here, if there is no specification after the time is that the aquisition of the vertical slice (STEREO), the duration of the volume is specified. There is usually a gap of a few minutes between the STEREO acquisition and the volume one. 
