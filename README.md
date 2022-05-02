# 1st Annual Hackathon (Project B)

Topic: **Scoring a sound recording**

+ Allow a therapist to score a sound recording (the output from Project A)
    + Should allow error analysis down to the phoneme level
+ Ideas to consider
    + Should you have them listen to just the audio first (prior to showing the attempted word or phrase)?
    + Is there a way to gamify it?
    + Should it be accompanied with a sound file demonstrating the correct or standard pronunciation?

## Included files

`/audio_files`

These are files in the formats .mp3, .wav, and .ogg of children attempting to say various words or phrases. See `audio_files.rb` for the complete list.

```ruby

male_25_words = []
male_62_words = []
female_24_words = []

files.each do |file|
  if file[:sex] == "male" && file[:age_in_months] == 62
    male_62_words << file[:word_phrase]
  elsif file[:sex] == "male" && file[:age_in_months] == 25
    male_25_words << file[:word_phrase]
  elsif file[:sex] == "female" && file[:age_in_months] == 24
    female_24_words << file[:word_phrase]
  end
end

puts "Female (24 months): #{female_24_words.join(", ")}"
puts "Count: #{female_24_words.length}"
puts "Male (25 months): #{male_25_words.join(", ")}"
puts "Count: #{male_25_words.length}"
puts "Male (62 months): #{male_62_words.join(", ")}"
puts "Count: #{male_62_words.length}"

```

## Example Pronunciations

`/example_pronunciations`

These are files in the formats .mp3, .wav, and .ogg of example pronunications for some of the same words as above.

+ [blue](https://en.wiktionary.org/wiki/File:en-us-blue.ogg)
+ [bus](https://en.wiktionary.org/wiki/File:en-us-bus.ogg)
+ [nose](https://en.wiktionary.org/wiki/File:en-us-nose.ogg)