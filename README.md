Approach:
   - Do not support pedal
   - Square all frequencies from the frequency map received from the fourier transform
   - Find closest note to each analysed frequency past a certain threshold.

   - Update working memory with note and associated start/end time: memory = {notename: [startTime, endTime=startTime]}
   - Continuously update the note's end time in memory with the current system time as long as the note is playing.
   - Once the note is no longer above the threshold, export the note to a CSV->Midi file.


CSV->Midi Converter:
   - Use py_midi_csv to convert from a csv file in py_midi_csv format to midi.



   
   - Update a log file with the note and associated state time: [notename]: [starttime,endtime=starttime]
   - Continuously update the [notename][endtime] variable with the current system time so long as the note is playingm
   - When the note stops, 