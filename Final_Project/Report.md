# Aerobic Heterotrophs and Autotrophic Nitrifiers Competition in Trickling Filters
### Zoe Maisel

## Introduction and Background
Trickling filters are used to treat biological oxygen demand (BOD) and nutrient rich wastewater. Trickling filters can be used in combined secondary treatment applications for BOD removal and nitrification in the same reactor, or as tertiary treatment reactors for nitrification. In combined secondary treatment applications, the main bacterium of interest are aerobic heterotrophs which degrade BOD and autotrophic nitrifiers which are responsible for nitrification. Aerobic heterotrophs consume influent carbon as an energy and carbon source while autotrophic nitrifiers consume $CO_2$ as a carbon source and inorganic nitrogen as an energy source.

Aerobic heterotrophs and autotrophic nitrifiers do not directly compete for energy sources, but they do compete for space, oxygen, and other nutrients that enter the biofilm from the influent waste. Heterotrophs can outcompete nitrifiers due to higher growth rates. Carbon to nitrogen (C/N) ratio, dissolved oxygen (DO) concentrations, and temperature are relevant factors for modeling microbial competition. BOD at high enough concentrations can inhibit nitrification.

Research on heterotroph and nitrifier competition has mostly employed empirical models to determine appropriate parameters for trickling filter operation. Maximum BOD influent loadings in the form of C/N ratios have been recommended based on field experiments, many of which were published by the US EPA ([U.S. EPA](https://nepis.epa.gov/Exe/ZyNET.exe/P1004T3S.TXT?ZyActionD=ZyDocument&Client=EPA&Index=1991+Thru+1994&Docs=&Query=&Time=&EndTime=&SearchMethod=1&TocRestrict=n&Toc=&TocEntry=&QField=&QFieldYear=&QFieldMonth=&QFieldDay=&IntQFieldOp=0&ExtQFieldOp=0&XmlQuery=&File=D%3A%5Czyfiles%5CIndex%20Data%5C91thru94%5CTxt%5C00000020%5CP1004T3S.txt&User=ANONYMOUS&Password=anonymous&SortMethod=h%7C-&MaximumDocuments=1&FuzzyDegree=0&ImageQuality=r75g8/r75g8/x150y150g16/i425&Display=hpfr&DefSeekPage=x&SearchBack=ZyActionL&Back=ZyActionS&BackDesc=Results%20page&MaximumPages=1&ZyEntry=1&SeekPage=x&ZyPURL), 1991).
# Need to add more sources in general

## Science Questions and Objectives
Design of trickling filters relies heavily on empirical models and observations. Using empirical models can lead to transferability issues, in that models derived for a specific reactor geometry, packing material, and influent may not apply to other treatment scenarios.  Inappropriate use of empirical models may lead to inefficient or unoptimized reactors and treatment schemes for combined BOD removal and nitrification trickling filters.

Using first-order fundamental models to understand trickling filter treatment would provide a more robust analysis of trickling filters, specifically competition between heterotrophs and nitrifiers. It is understood that heterotrophs can outcompete nitrifiers because of the higher growth yield for heterotrophs, and because organic carbon is a stronger electron donor than inorganic nitrogen. A model for metabolic interactions that focuses on competition for oxygen would give more insight into trickling filter operation .

## Mathematical Modeling/Theoretical Considerations
Plan:

Metabolic
How much oxygen, what is the total BOD?
1. Determine representative wastewater organics from small/household sources. Characteristic organic matter and express  electron basis. Use half reaction provided in problem set 6 for ww.
2. Determine typical BOD and DO.
3. Half reaction. BOD e- donor for heterotroph, ammonium as electron donor ratio. How much oxygen is required for each
3. Determine relevant biomass yield and oxygen requirement equations for heterotrophs (stoichiometry).

Determine overall growth reaction for heterotrophs and nitrifier using fe and fs. use that to determine yield of each biomass.
Ue delta G value which are more thermodynamically favorable.

---------------------

#### Definition of variables
$ \Delta G^{o'}$: Gibbs Standard Free Energy Equation at pH = 7.0
$ R_e $: Energy reaction
$ R_s $: Synthesis reaction
$ f_e^o $: Theoretical fraction of electrons allocated to energy metabolism
$ f_s^o $: Theoretical fraction of electrons allocated to cell synthesis
$ f_e $
$ f_s $
$ A $: Number of electron equivalents of electon donor converted to energy per electron of cells synthsized
$ \Delta G_p $
$ \Delta G_{pc} $
$ \Delta G_r $
$ \epsilon $
$ n $
$ f_d $
$ b $
$ \theta_x^{min} $
$ \theta_x^{design} $
$ SF $
$ correction $


---------------------
#### Aerobic Heterotrophs:

Electron donor: $ C_{10}H_{19}O_{3}N $
Electron acceptor: $ O_2 $
Nitrogen source: $ NH_4^+ $

#####Energy equation:
######Half-reaction for domestic wastewater with biodegradable organics as an electron donor:
$ \frac{1}{50}C_{10}H_{19}O_{3}N + \frac{9}{25}H_2O = \frac{9}{50}CO_2 + \frac{1}{50}NH_4^+ + \frac{1}{50}HCO_3^- + H^+ + e^-$

where $ \Delta G^{o'} = -31.8 \frac{KJ}{e^-eq}$

######Half-reaction for reduction of oxygen:
$ \frac{1}{4}O_2 + H^+ + e^-= \frac{1}{2}H_2O $

where $ \Delta G^{o'} = -78.72 \frac{KJ}{e^-eq}$

##### Total energy equation, $R_e$:
$ \frac{1}{50}C_{10}H_{19}O_{3}N +\frac{1}{4}O_2 = \frac{9}{50}CO_2 + \frac{1}{50}NH_4^+ + \frac{1}{50}HCO_3^- + \frac{7}{50}H_2O $

where $ \Delta G^{o'} = -110.52 \frac{KJ}{e^-eq}$

#####Cell synthesis equation:
######Half-reaction for domestic wastewater with biodegradable organics as an electron donor:
$ \frac{1}{50}C_{10}H_{19}O_{3}N + \frac{9}{25}H_2O = \frac{9}{50}CO_2 + \frac{1}{50}NH_4^+ + \frac{1}{50}HCO_3^- + H^+ + e^-$

where $ \Delta G^{o'} = -31.8 \frac{KJ}{e^-eq}$

######Half-reaction for cell synthesis using ammonium as nitrogen source:
$ \frac{1}{5}CO_2 + \frac{1}{20}HCO_3^- + \frac{1}{20}NH_4^+ + H^+ + e^- = \frac{1}{20}C_5H_7O_2N + \frac{9}{20}H_2O $

##### Total synthesis equation, $R_s$:
$ \frac{1}{50}C_{10}H_{19}O_{3}N + \frac{2}{100}CO_2 + \frac{3}{100}HCO_3^- + \frac{3}{100}NH_4^+= \frac{1}{20}C_5H_7O_2N + \frac{9}{100}H_2O$

#####Calculation of $f_e$ and $f_s$
$ A = \frac{-(\frac{\Delta G_p}{\epsilon^n} + \frac{\Delta G_{pc}}{\epsilon})}{\epsilon \Delta G_r} $

$ \Delta G_r  = \Delta G_{R_e} = -110.52 \frac{KJ}{e^-eq} $
$ \Delta G_p  = \Delta G_{pyruvate} - \Delta G_{C-source} = (35.09-31.8)\frac{KJ}{e^-eq} = 3.29 \frac{KJ}{e^-eq} $
$ \Delta G_p > 0  ∴  n=1 $
$ \Delta G_{pc} = 18.8 \frac{KJ}{e^-eq} $
$ \epsilon ≈ 0.6 $

$ A_{heterotroph} = 0.555 $
$ f_s^o  = \frac{1}{1+A} = 0.643 $
$ f_e^o  = 1-f_s^o = 0.357 $

Correction factor to account for aerobic heterotroph cell decay = $ \frac{1+(1-f_d)(b \theta_x)}{1+b \theta_x} $

Page 309, Rittman and McCarty
$ f_d = 0.8 $
$ b = 0.15 \frac{1}{day} $
$ \theta_x^{min} = 2.8 $ days, chosen from $ \theta_x^{min}$ for ammonium oxidizers at $10^o C $, page 472, Rittman and McCarty
$ SF = 2 $
$ \theta_x^{design} = 5.6 $ days

$ correction = 0.635 $
$ f_s = correction*f_s^o  = 0.408 $
$ f_e = 1-f_s  = 0.591 $

##### Total reaction equation, R
Only taking into account $O_2$, $C_{10}H_{19}O_{3}N$, $NH_4^+$, and $C_5H_7O_2N$:

$ f_sR_s:  0.00816C_{10}H_{19}O_{3}N + 0.01224NH_4^+= 0.0204C_5H_7O_2N $
$ f_eR_e: 0.01182C_{10}H_{19}O_{3}N + 0.14775O_2 = 0.01182NH_4^+  $

$ R: 0.01998C_{10}H_{19}O_{3}N + 0.14775O_2 + 0.00042NH_4^+ = 0.0204C_5H_7O_2N $

From this equation for heterotrophic metabolism and cell synthesis, 0.14775 $mol O_2$ is required for 1 $e^-eq$.

##### Expected yield
$ Y = \frac{biomass_{mass}}{e^-donor_{mass}} $

---------------------
####Aerobic nitrifiers:
Electron donor: $ NH_4^+ $
Electron acceptor: $ O_2 $
Nitrogen source: $ NH_4^+ $

#####Energy equation:
######Half-reaction for reduction of ammonium:
$ \frac{1}{8}NH_4^+ + \frac{3}{8}H_2O = \frac{1}{8}NO_3^- + \frac{5}{4}H^+ + e^- $

where $ \Delta G^{o'} = 35.11 \frac{KJ}{e^-eq}$

######Half-reaction for reduction of oxygen:
$ \frac{1}{4}O_2 + H^+ + e^-= \frac{1}{2}H_2O $

where $ \Delta G^{o'} = -78.72 \frac{KJ}{e^-eq}$

##### Total energy equation, $R_e$:
$ \frac{1}{8}NH_4^+ + \frac{1}{4}O_2  = \frac{1}{8}NO_3^- + \frac{1}{4}H^+ + \frac{1}{8}H_2O$

#####Cell synthesis equation:
######Half-reaction for reduction of ammonium:
$ \frac{1}{8}NH_4^+ + \frac{3}{8}H_2O = \frac{1}{8}NO_3^- + \frac{5}{4}H^+ + e^- $

where $ \Delta G^{o'} = 35.11 \frac{KJ}{e^-eq}$

######Half-reaction for cell synthesis using ammonium as nitrogen source:
$ \frac{1}{5}CO_2 + \frac{1}{20}HCO_3^- + \frac{1}{20}NH_4^+ + H^+ + e^- = \frac{1}{20}C_5H_7O_2N + \frac{9}{20}H_2O $

##### Total synthesis equation, $R_s$:
$ \frac{1}{5}CO_2 + \frac{1}{20}HCO_3^- + \frac{7}{40}NH_4^+   = \frac{1}{20}C_5H_7O_2N + \frac{1}{8}NO_3^- + \frac{3}{40}H_2O + \frac{1}{4}H^+$

---------------------

4. Determine relevant biomass yield and oxygen requirement equations for nitrifiers (stoichiometry).
5. Use \delta G values to analyze the likelihood of oxygen being used by heterotroph or nitrifier.
6. Set a criteria for minimum nitrification treatment and determine what level of DO is needed to ensure that nitrification happens.
7. Use that to determine the maximum influent BOD.

Kinetic
Model competition for oxygen using the dual substrate model
Find k values

## Work Plan and Expected Results
