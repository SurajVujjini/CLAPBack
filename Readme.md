# CLAPBack

CLAPBack is a project to explore emotional music search using audio, lyrics, and MIDI.  
The idea is to let people type something like “songs that feel like heartbreak in spring” and actually get back music that matches that emotional feel.
**This is a demo for the question asked as part of the recuiting process for a positon at Tamber.**

## Mission Statement

Build a search system that understands the emotional feel of music, not just genre or tempo, by combining features from:

- Audio (using CLAP)
- Lyrics (using Sentence-BERT)
- MIDI (tempo, pitch, note density with pretty_midi)


## File Structure

- `notebook.ipynb`  
  Main Jupyter notebook containing the full pipeline: data loading, preprocessing, embedding generation, search, and validation.

- `audio_midi_lyrics/`  
  Folder containing the dataset subset: 50 audio files (.mp3), lyrics (.txt), and MIDI files (.mid), all matched by ID.

- `Embeddings/`  
  Stores the generated embedding vectors (`.npy` files) and song IDs after processing.

- `Readme.md`  
  This README file with project overview, structure, progress, and next steps.


## Current Progress

- Collected a subset of 50 songs from the 2013 MIREX-like Mood Dataset, each with audio, lyrics, and MIDI
- Embedded audio, lyrics, and MIDI features into a single combined vector
- Built a cosine similarity search to match user queries to songs
- Added query support through the terminal
- Visualized song embeddings in 2D using t-SNE to check for clustering

## Possible Next Steps

- Build a small interface to let users type a query, see results, and listen to tracks
- Train on the full dataset  instead of just 50 songs. 
- Include more emotionally diverse music (not just romantic or breakup songs (FacePalm.gif!))
