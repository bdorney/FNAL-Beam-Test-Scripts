# FNAL-Beam-Test-Scripts
note: doubleGausFit_withHistParameter.C contains the function to do double Gausian fit. The scritps that need it already have it included.

step 1: select events.

  use SelectTrackerEvents.C, can be changed to include selecting GEM events

step 2: alignment of trackers.

  use AlignTrackers_Shift.C, AlignTrackers_shift_rotate.C, AlignTrackers_optimizeRotation.C

  each script has iterations, for the third script, when optimizing rotation angles, optimize one detector one time,

  in other words, the iteration quantity is the angle for one tracker, the other angles are fixed

step 3: alignment GEM detector to trackers

  use AlignGEM_XYoffsets.C,

  after this script, will get some text files, then

  draw_allX_vs_Y.C, draw_allY_vs_X.C, draw_XY_Offsets.C can be used for them

  use AlignGEM_rotate.C, and draw_fixXY_vs_rotationAngle.C

then resolution can be calculated with AlignGEM_rotate.C by setting all X,Y offsets and angle, and do not doing iteration.  
