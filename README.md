# 🌳 Tree Species Identification Trainer

A comprehensive web-based training tool for professional tree identification, designed for PTI (Professional Tree Inspection) certification preparation.

## 📋 Overview

This trainer helps tree surveyors and arborists master tree identification across:
- **Multiple seasons** (winter dormant and summer in-leaf observations)
- **Different life stages** (juvenile through veteran specimens)
- **Two difficulty levels** (species and variety/cultivar identification)
- **Major UK tree groups** (Maple, Oak, Ash, Birch, Cherry, Rowan, Lime, Beech, Hornbeam, and more)

## 🚀 Quick Start

### Local Setup

1. **Download or clone** this repository
2. **Open** `index.html` in a modern web browser
3. **Start learning!** The trainer will load the tree database automatically

That's it! No installation, no dependencies, no build process required.

### Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- Local file access (or serve via simple HTTP server)

### Optional: Local Server

If you prefer to serve the files via HTTP:

```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (with http-server installed)
npx http-server

# PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

## 🎮 Features

### Two-Level Learning System

**Species Level Mode**
- Identify genus and species (e.g., "Acer platanoides")
- Master the fundamental 28 tree species
- Build foundation knowledge

**Variety Level Mode**
- Identify specific cultivars (e.g., "Acer platanoides 'Crimson King'")
- Advanced identification challenge
- Perfect for professional tree surveyors

### Progressive Scoring System

- **10 points** - Perfect spelling and identification
- **8 points** - Minor spelling variations (very close)
- **6 points** - Species correct, variety wrong (variety mode)
- **4 points** - Genus only correct
- **0 points** - Incorrect genus

### Intelligent Filtering

**Season Filters**
- All Seasons (mixed winter/summer observations)
- Winter Only (bark, buds, form, twigs)
- Summer Only (leaves, flowers, fruit, form)

**Group Filters**
- All Groups (full database)
- Filter by genus (Maple, Oak, Ash, etc.)
- Focus practice on challenging groups

**Life Stage Filters**
- All Stages
- Juvenile features
- Mature features
- Veteran characteristics

### Learning Notes System

After each answer, receive comprehensive learning notes:

- **Why This Tree?** - Context and importance
- **Key Differentiators** - Comparison with similar species using the proven format:
  - "SIMILAR SPECIES: differences..."
  - "UNIQUE TO [THIS TREE]: diagnostic features"
- **Seasonal Notes** - What to observe in different seasons
- **Identification Tips** - Memory aids and field shortcuts

### Progress Tracking

Your statistics are automatically saved:
- Total questions answered
- Average score
- Accuracy percentage
- Current streak
- Perfect answers count

## 📊 Database Structure

### Current Database

The `tsv/trees_data.tsv` file contains **28 tree species** covering:

- **Maple (Acer)** - 4 species including varieties
- **Oak (Quercus)** - 2 species
- **Ash (Fraxinus)** - 1 species
- **Birch (Betula)** - 2 species
- **Cherry (Prunus)** - 2 species
- **Rowan/Whitebeam (Sorbus)** - 2 species
- **Lime (Tilia)** - 2 species
- **Beech (Fagus)** - 2 varieties
- **Hornbeam (Carpinus)** - 1 species
- **Plane (Platanus)** - 1 species
- **Pine (Pinus)** - 1 species
- **Alder (Alnus)** - 1 species
- **Hawthorn (Crataegus)** - 1 species
- **Crab Apple (Malus)** - 1 species
- **Yew (Taxus)** - 2 varieties
- **Willow (Salix)** - 1 species
- **Poplar (Populus)** - 1 species
- **Ginkgo** - 1 species

### TSV Format

The database uses tab-separated values (TSV) for easy editing in spreadsheet software:

```
id	active	latinName	commonName	varietyName	speciesGroup	winterBark	winterBuds	...
1	YES	Acer platanoides	Norway Maple		Maple	Dark grey bark...
```

**Key Columns:**
- `active` - YES/NO flag to enable/disable species
- `latinName` - Full Latin binomial (Genus species)
- `varietyName` - Cultivar name (if applicable)
- `winterBark/Buds/Form/Twigs` - Winter observations
- `summerLeaf/Flower/Fruit/Form` - Summer observations
- `juvenileFeatures/matureFeatures/veteranFeatures` - Life stage notes
- `whyThisTree` - Contextual information
- `keyDifferentiators` - Comparison with similar species
- `seasonalNotes` - Season-specific observations
- `identificationTips` - Memory aids and shortcuts

## ✏️ Customizing the Database

### Adding New Trees

1. Open `tsv/trees_data.tsv` in Excel, Google Sheets, or any text editor
2. Add a new row with all required columns
3. Set `active` to `YES`
4. Fill in observations for winter and summer
5. **Crucially** - write excellent differentiators following this format:

```
SIMILAR SPECIES A: key differences. SIMILAR SPECIES B: other differences. 
UNIQUE TO [YOUR TREE]: diagnostic features that make it unmistakable.
```

6. Save the file (maintain tab-separated format)
7. Refresh the trainer - new tree appears immediately!

### Editing Existing Trees

Simply edit the TSV file and refresh the browser. No code changes needed.

### Disabling Trees

Set `active` to `NO` to temporarily remove a tree from the trainer.

## 🎓 Educational Philosophy

This trainer is based on proven learning principles:

1. **Active Recall** - Type the answer from memory
2. **Spaced Repetition** - Random selection encourages repeated exposure
3. **Immediate Feedback** - See correct answer and learn why
4. **Comparative Learning** - Differentiators highlight key differences
5. **Multi-Modal Information** - Winter vs summer, different life stages
6. **Progressive Difficulty** - Species mode before variety mode

## 💡 Tips for Effective Learning

### For Beginners

1. Start with **Species Level** mode
2. Use **Group Filter** to focus on one genus at a time
3. Master winter identification first (fewer variables)
4. Read ALL the learning notes after each question
5. Practice daily for 15-20 minutes

### For Advanced Users

1. Switch to **Variety Level** mode
2. Use **All Seasons** filter for mixed challenges
3. Focus on genera with many similar species (Acer, Sorbus, Tilia)
4. Pay special attention to differentiators
5. Practice in the field after training sessions

### Memory Techniques

The database includes Latin etymology tips:
- *Acer platanoides* = plane-like maple
- *Quercus petraea* = oak of rocky places
- *Betula pendula* = pendulous birch
- *Populus tremula* = trembling poplar

## 📱 Browser Compatibility

Tested and working on:
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

## 🔒 Privacy

All progress data is stored locally in your browser using `localStorage`. No data is sent to any server. Your learning progress stays on your device.

## 🤝 Contributing

### Adding More Species

The database currently includes 28 species but can easily expand to 80+. Priority additions:

- More Sorbus varieties (12+ species available)
- Additional Prunus species
- More cultivars of common street trees
- Regional specialties

### Improving Differentiators

The quality of the differentiators directly impacts learning effectiveness. When contributing:

1. Compare within genus first (all Acer together)
2. Note cross-genus similarities (Hornbeam vs Beech)
3. Always end with "UNIQUE TO [SPECIES]:" section
4. Use uppercase for genus names in comparisons
5. Be specific and diagnostic

## 📚 Related Resources

- [British Tree Identification](https://www.woodlandtrust.org.uk/trees-woods-and-wildlife/british-trees/)
- [PTI Certification](https://lantra.co.uk)
- [Tree ID Apps] - Use alongside this trainer for field practice

## 📄 License

This educational tool is provided as-is for personal learning and professional development.

## 🌳 Acknowledgments

Built following the proven fungi trainer model, with adaptations for the unique challenges of tree identification across seasons and life stages.

## 🐛 Troubleshooting

**Trees not loading?**
- Check browser console for errors
- Verify `tsv/trees_data.tsv` exists
- Ensure TSV file is tab-separated (not spaces or commas)

**Stats not saving?**
- Ensure browser allows localStorage
- Check you're not in private/incognito mode
- Try a different browser

**Filters not working?**
- Refresh the page
- Check console for JavaScript errors
- Verify your TSV data has the correct column headers

---

**Happy learning! 🌳 Master those tree identifications!**
