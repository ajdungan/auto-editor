
 # --format
--format
the format youtube-dl uses to when downloading a url.
* type: str
* default: bestvideo[ext=mp4]+bestaudio[ext=m4a]/mp4
* group: urlOps

 # --output_dir
--output_dir
the directory where the downloaded file is placed.
* type: str
* default: None
* group: urlOps

 # --check_certificate
--check_certificate
check the website certificate before downloading.
* type: flag
* group: urlOps

 # --machine_readable_progress
--machine_readable_progress
set progress bar that is easier to parse.
* type: flag
* group: progressOps

 # --no_progress
--no_progress
do not display any progress at all.
* type: flag
* group: progressOps

 # --force_fps_to
--force_fps_to
manually set the fps value for the input video if detection fails.
* type: float
* default: None
* group: metadataOps

 # --force_tracks_to
--force_tracks_to
manually set the number of tracks auto-editor thinks there are.
* type: int
* default: None
* group: metadataOps

 # --video_bitrate
--video_bitrate, -vb
set the number of bits per second for video.
* type: str
* default: unset
* group: exportMediaOps

 # --audio_bitrate
--audio_bitrate, -ab
set the number of bits per second for audio.
* type: str
* default: unset
* group: exportMediaOps

 # --sample_rate
--sample_rate, -r
set the sample rate of the input and output videos.
* type: sample_rate_type
* default: None
* group: exportMediaOps

 # --video_codec
--video_codec, -vcodec
set the video codec for the output media file.
* type: str
* default: uncompressed
* group: exportMediaOps

 # --audio_codec
--audio_codec, -acodec
set the audio codec for the output media file.
* type: str
* default: None
* group: exportMediaOps

 # --preset
--preset, -p
set the preset for ffmpeg to help save file size or increase quality.
* type: str
* default: unset
* Choices: ultrafast, superfast, veryfast, faster, fast, medium, slow,
slower, veryslow, unset
* group: exportMediaOps

 # --tune
--tune, -t
set the tune for ffmpeg to compress video better in certain
circumstances.
* type: str
* default: unset
* Choices: film, animation, grain, stillimage, fastdecode, zerolatency,
none, unset
* group: exportMediaOps

 # --constant_rate_factor
--constant_rate_factor, -crf
set the quality for video using the crf method.
* type: str
* default: unset
range: 0 to 51
* group: exportMediaOps

 # --dilates
--dilates, -d
set how many times a frame is dilated before being compared.
* type: int
* default: 2
range: 0 to 5
* group: motionOps

 # --width
--width, -w
scale the frame to this width before being compared.
* type: int
* default: 400
range: 1 to Infinity
* group: motionOps

 # --blur
--blur, -b
set the strength of the blur applied to a frame before being compared.
* type: int
* default: 21
range: 0 to Infinity
* group: motionOps

 # --export_as_audio
--export_as_audio, -exa
export as a WAV audio file.
* type: flag

 # --export_to_premiere
--export_to_premiere, -exp
export as an XML file for Adobe Premiere Pro instead of outputting a
media file.
* type: flag

 # --export_to_resolve
--export_to_resolve, -exr
export as an XML file for DaVinci Resolve instead of outputting a media
file.
* type: flag

 # --export_to_final_cut_pro
--export_to_final_cut_pro, -exf
export as an XML file for Final Cut Pro instead of outputting a media
file.
* type: flag

 # --export_as_json
--export_as_json
export as a JSON file that can be read by auto-editor later.
* type: flag

 # --export_as_clip_sequence
--export_as_clip_sequence, -excs
export as multiple numbered media files.
* type: flag

 # --render
--render
choice which method to render video.
* type: str
* default: auto
* Choices: av, opencv, auto

 # --scale
--scale
scale the output media file by a certian factor.
* type: float_type
* default: 1

 # --zoom
--zoom
set when and how a zoom will occur.
The arguments are: start,end,start_zoom,end_zoom,x,y,inter,hold
There must be at least 3 comma args. x and y default to centerX and centerY
The default interpolation is linear.
* type: zoom_type
* default: None

 # --rectangle
--rectangle
overlay a rectangle shape on the video.
The arguments are: start,end,x1,y1,x2,y2,color,thickness
There must be at least 6 comma args. The rectangle is solid if thickness is
not defined.
The default color is 
 #000.
* type: rect_type
* default: None

 # --background
--background
set the color of the background that is visible when the video is moved.
* type: str
* default: 
 #000

 # --mark_as_loud
--mark_as_loud
the range that will be marked as "loud".
* type: range_type
* default: None

 # --mark_as_silent
--mark_as_silent
the range that will be marked as "silent".
* type: range_type
* default: None

 # --cut_out
--cut_out
the range of media that will be removed completely, regardless of the
value of silent speed.
* type: range_type
* default: None

 # --set_speed_for_range
--set_speed_for_range
set an arbitrary speed for a given range.
The arguments are: speed,start,end
* type: speed_range_type
* default: None

 # --motion_threshold
--motion_threshold
how much motion is required to be considered "moving"
* type: float_type
* default: 0.02
range: 0 to 1

 # --edit_based_on
--edit_based_on
decide which method to use when making edits.
* type: str
* default: audio
* Choices: audio, motion, not_audio, not_motion, audio_or_motion,
audio_and_motion, audio_xor_motion, audio_and_not_motion,
not_audio_and_motion, not_audio_and_not_motion

 # --cut_by_this_audio
--cut_by_this_audio, -ca
base cuts by this audio file instead of the video's audio.
* type: file_type
* default: None

 # --cut_by_this_track
--cut_by_this_track, -ct
base cuts by a different audio track in the video.
* type: int
* default: 0
range: 0 to the number of audio tracks minus one

 # --cut_by_all_tracks
--cut_by_all_tracks, -cat
combine all audio tracks into one before basing cuts.
* type: flag

 # --keep_tracks_seperate
--keep_tracks_seperate
don't combine audio tracks when exporting.
* type: flag

 # --my_ffmpeg
--my_ffmpeg
use your ffmpeg and other binaries instead of the ones packaged.
* type: flag

 # --version
--version
show which auto-editor you have.
* type: flag

 # --debug
--debug, --verbose, -d
show debugging messages and values.
* type: flag

 # --verbose
--debug, --verbose, -d
show debugging messages and values.
* type: flag

 # --show_ffmpeg_debug
--show_ffmpeg_debug
show ffmpeg progress and output.
* type: flag

 # --quiet
--quiet, -q
display less output.
* type: flag

 # --combine_files
--combine_files
combine all input files into one before editing.
* type: flag

 # --preview
--preview
show stats on how the input will be cut.
* type: flag

 # --no_open
--no_open
do not open the file after editing is done.
* type: flag

 # --min_clip_length
--min_clip_length, -mclip
set the minimum length a clip can be. If a clip is too short, cut it.
* type: frame_type
* default: 3
range: 0 to Infinity

 # --min_cut_length
--min_cut_length, -mcut
set the minimum length a cut can be. If a cut is too short, don't cut
* type: frame_type
* default: 6
range: 0 to Infinity

 # --output_file
--output_file, --output, -o
set the name(s) of the new output.
* type: str
* default: None

 # --output
--output_file, --output, -o
set the name(s) of the new output.
* type: str
* default: None

 # --silent_threshold
--silent_threshold, -t
set the volume that frames audio needs to surpass to be "loud".
* type: float_type
* default: 0.04
range: 0 to 1

 # --silent_speed
--silent_speed, -s
set the speed that "silent" sections should be played at.
* type: float_type
* default: 99999
range: Any number. Values <= 0 or >= 99999 will be cut out.

 # --video_speed
--video_speed, --sounded_speed, -v
set the speed that "loud" sections should be played at.
* type: float_type
* default: 1.0
range: Any number. Values <= 0 or >= 99999 will be cut out.

 # --sounded_speed
--video_speed, --sounded_speed, -v
set the speed that "loud" sections should be played at.
* type: float_type
* default: 1.0
range: Any number. Values <= 0 or >= 99999 will be cut out.

 # --frame_margin
--frame_margin, -m
set how many "silent" frames of on either side of "loud" sections be
included.
* type: frame_type
* default: 6
range: 0 to Infinity
