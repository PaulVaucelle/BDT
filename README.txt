//////////////////////////////////////////////////////////////////////////////////////////
// This Git is gathering every BDT/DNN used in the analysis codes TrackingPerf/FlyingTop//
//----------------------------------------------------------------------------------------
// It is split between MVA methods trained on RECO or MINIAOD
// then between benchmarks. In previous studies, it was shown that any BDT with any benchmarks used for training 
// works for all other benchmark (= Signal Efficiency and Bkg efficiency).  The choice was made to use the 50 cm becnhmark 
// as the main sample for training and test.
// Pls find below the optimal cut for the MVA methods when available
// If no value is given, an optimal cut of 0 is more than fine in all cases
//////////////////////////////////////////////////////////////////////////////////////////

The overall Signal Efficiency is about 85% for a bkg Efficiency of 20-15%.

// ./RECO/50cm/ :
- withnhits:-0.0401 (Version used during the internship ***with less training***, doesn't take into account b and c jets => more displacement)
- FromBC :-0.1083 (is not good atm)
- HighPurity :-0.1456 (MINIAOD is only using HighPurityTracks)
- NewSignal : 0.0327 (takes into account b and c jets) ////*****best BDT******////
- sansntrk10_avecHP : -0.0067 (used for lostTracks collection for MINIAOD)
- 50cm : 0.0057 (Version used during the internship ***with better training***, doesn't take into account b and c jets => more displacement)
- sansalgo : -0.0815 (MINIAOD does not have access to algo)
- DNN : NAN (not used since same values of S_eff and Bkg_eff as the BDTs)


//**Last Update : 19/12/2022**//
Paul