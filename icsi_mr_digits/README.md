# ICSI Meeting Recorder Digits

This is a subset of the ICSI Meeting Corpus which corresponds to digit sequences read by participants at the end of many of the meetings.  The recordings were captured by 4 PZM microphones, although the data in this directory corresond only to one microphone, c2.

The original waveforms were stored in NIST wave format with shorten encoding, which can be a bit cumbersome to handle.  A script, go.extract.waveforms, was provided by Marc Ferras to extract individual waveforms into NIST wave format (note - not the same as Microsoft WAV format, which is more common these days).  The script is provided in the docs directory for reference

The files have the following naming conventions:

```
#  Bmr002-me011-c2-u1-7-0196-488o7o1.wav
#
#      Meeting id: Bmr002     (Berkeley meeting Recorder meeting 002)
#      Speaker id: me011      (Male, native English speaker, 011)
#          Mic id: c2         (Crown PZM desktop microphone)
#   Transmit type: u1         (Unknown wired type)
#         Channel: 7
# Transcript line: 0196
#   Transcription: 488o7o1    (Four Eight Eight Oh Seven Oh One)
```

The channel corresponds to where the microphone was placed on the table, which can be looked up in seatingchart.txt.

This extracted piece of the ICSI Meeting Recorder data (digits only) was provided to Ohio State under a CC-BY-SA-4.0 license, and the segmentation adaptation is provided by Eric Fosler-Lussier under the same CC-BY-SA-4.0 license.

A note on training/test sets: for ease of division, the "Bro" (Robustness) meetings are used as test utterances; there are two speakers that overlap, so they have been removed and added to the training set.  This is really not the best way to do a training/test split but does try to balance meeting split while not having overlapping speakers.  Note that the data are very much not gender balanced.