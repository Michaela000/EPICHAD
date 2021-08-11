# Results & outcomes


## Hypothesis

### Hypothesis 1
- Children have higher frequency oscillation than adult patients

### Hypothesis 2
- Children dont have higher frequency oscillation than adult patients 


## Results

**1. ICA outcomes** 

For artifact reduction, we used an Independent Component Analysis (ICA) with an added low frequency filter of 1.0 Hz. To fit the ICA and for vizualisation, we used 8 components that are shown in the following figures. 

_1.1 ICA outcome in Adult:_
![Adult_ICA](https://user-images.githubusercontent.com/82948946/126979246-936a2803-0586-4ee9-bb31-379556276ec2.png)

This ICA-picture shows the 8 different components from an adult subject. The activation pattern is very different in each component: e.g. the first component ICA000 shows high activation in the frontal area near the eyes. Usually you would exclude this component because of artifacts due to eye movement, but in this case it was still considered an important component. There are a few components that are difficult to analyze because they are not focused (e.g: ICA005, ICA002). In ICA004 is an higher activity in the occipital lobe. Overall it can be seen, that the activity is mostly focused on the frontal (ICA000, ICA001), parietal (ICA001, ICA007) and occipital (ICA004, ICA006) lobe.  

_1.2 ICA outcome in Children:_
![Child_ICA](https://user-images.githubusercontent.com/82948946/126979253-fec58dbc-fead-4fdc-bbb9-7ab36bb9f425.png)
This ICA-picture shows the 8 different compoenents from a children subject. A lot of the components are not focused and are therefore difficult to describe (e.g: ICA000, ICA004). Most of the activation is located at the frontal (ICA003) and temporal (ICA002, ICA006) lobe. 

**2. Topomap outcomes without vmax and vmin**


_2.1 Topomap outcome in adults without vmax and vmin_ 

![Adult_Topomap_without_lim](https://user-images.githubusercontent.com/82948946/126979376-4395b592-351b-4aad-9203-f9c7c67946b7.png)

These topomaps show the brain activity of an adult siubject in Delta (0-4 Hz), Theta (4-8 Hz), Alpha (8-12 Hz), Beta (12-20 Hz) and Gamma (30-45Hz) bands in order to show where the activity is mostly focused. Delta shows mostly activation in the temporal and occipital lobe while Theta and Alpha have mostly activation in the frontal lobe. The last two bands (Beta and Gamma) indicate that nearly all actitivy is located at the temporal lobes.
It is very important to mention the different scales that are shown here. Delta reaches from 0.8-0.8; Theta from 0.0-0.1 and Alpha/Beta and Gamma from 0.0-0.0. These scales are different for all subjects, therefore the next step would be to define vmin and vmax for both groups individually.

_2.2 Topomap outcome in children without vmax and vmin_

![Child_Topomap_without_lim](https://user-images.githubusercontent.com/82948946/126979387-676bd9f8-0a97-4229-beda-18eeb1103a5b.png)

These topomaps show the brain activity of a child subject in Delta (0-4 Hz), Theta (4-8 Hz), Alpha (8-12 Hz), Beta (12-20 Hz) and Gamma (30-45) bands in order to show where the activity is mostly focused. Delta shows most of its activity in the occipital lobe. This subject has the same scale as the adult in the previous figure (2.1), therefore we can compare these results with each other. In this case, adults have more activity in the frontal to temporal lobes than in children. Theta (mostly frontal), Alpha (mostly frontal), Beta (mostly temporal) and Gamma (mostly temporal) are very similar to the adult subject. The only difference is, that children seem to have overall an higher activity compared to the adult subject (exception in this case Delta). Please remeber, that these are only two subjects out of 30. Therefore, it is very difficult to compare the topomaps if they are not scaled accordingly.   



**3. Topomap outcomes for vmax and vmin**


_3.1 Topomap outcome in Adults: Delta 0.7-0.9; Theta 0.0-0.2; Alpha/Beta/Gamma 0.0-0.1_

![Topomap_Adult](https://user-images.githubusercontent.com/82948946/126980285-4da35307-7e2d-47f0-8eb7-679ba255c8c9.PNG)

This adult-topomap shows the activity division in the same subject as in figure 2.1, but with an averaged scale for all adult subjects. The bigegst difference is Delta, which now has a range from 0.7-0.9. It can be seen, that Delta has again a higher overall activity than Theta, Alpha, Beta and Gamma. The activity is a little bit higher in the occipital lobe, than in the frontal lobe, but overall it is similar. From 4-8 Hz (Theta), there is also some activity mostly frontal and temporal, but please take notice of the scale (Delta from 0.7-0.9 while Theta goes from 0.0-0.2). 




_3.2 Topomap outcome in Children: Delta 0.5-0.9; Theta 0.0-0.2; Alpha/Beta/Gamma 0.0-0.1_

![Topomap_Child](https://user-images.githubusercontent.com/82948946/126980301-cf361820-703b-48da-b4d7-6478e3eadfe9.PNG)

This children-topomap shows the activity division in the same subject as in figure 2.2, but with an averaged scale for all children. The scale of Delta marks the biggest difference to before (before: 0.8-0.8 and now it goes from 0.5-0.9). There is an overall stronger activity in the whole brain in Delta if you compare it to the adult-topomap (3.1). But in contrast to that, there is a similar pattern for Theta, Alpha, Beta and Gamma. Please take notice of the different scales for Delta (Children: 0.5-0.9 and Adults: 0.7-0.9). So even, if the scale is larger, you have a higher activation and therefore, higher frequency oscillation. This is our prove of Hypothesis 1!
   



