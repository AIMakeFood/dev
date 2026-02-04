# Recipe Images Setup Instructions

## Status: Phase 1 Code Changes Complete ✓

The code has been updated to properly handle recipe images:
- ✅ Placeholder path fixed in `/app/(dashboard)/recipes/page.tsx`
- ✅ RecipeCard component now displays images
- ✅ ATTRIBUTION.md template created

## Required Action: Download Images from Freepik

You need to download the following images to complete the setup:

### 1. Create Placeholder Image (CRITICAL)

**File needed:** `placeholder-recipe.jpg`

**Options:**
- **Option A (Quick):** Copy one of the existing images as placeholder:
  ```bash
  cp "/Volumes/Untitled/Projects/AIMakeFood/web-app/public/images/recipes/high-angle-tasty-truffle-recipe_23-2149525124.jpg" "/Volumes/Untitled/Projects/AIMakeFood/web-app/public/images/recipes/placeholder-recipe.jpg"
  ```

- **Option B (Better):** Download a generic food/kitchen image from Freepik:
  1. Go to https://www.freepik.com/
  2. Search for "food preparation" or "cooking ingredients"
  3. Download a neutral, appetizing image
  4. Optimize to 1200x800px, save as `placeholder-recipe.jpg`

### 2. Download Additional Recipe Images (Recommended)

Download 10-15 diverse food images from Freepik to enhance recipe display:

**Suggested searches on Freepik:**
- Italian: "pasta marinara", "italian food"
- Asian: "stir fry vegetables", "asian cuisine"
- Mexican: "tacos", "mexican food platter"
- American: "classic burger", "american bbq"
- Mediterranean: "greek salad", "mediterranean dish"
- Indian: "chicken curry", "indian food"
- French: "ratatouille", "french cuisine"
- Japanese: "sushi roll", "japanese food"
- Chinese: "fried rice", "chinese dish"
- Thai: "pad thai", "thai food"

**Naming convention:**
- Format: `[cuisine]-[dish-type]-[description].jpg`
- Examples: `italian-pasta-marinara.jpg`, `asian-stirfry-vegetables.jpg`

**Image specifications:**
- Size: 1200x800px (3:2 ratio)
- Format: JPG or WebP
- Quality: 85% compression
- Target file size: ~150KB

### 3. Update ATTRIBUTION.md

After downloading each image:
1. Open `ATTRIBUTION.md`
2. Add the Freepik URL for each image
3. Add the author name
4. Save the file

Example:
```markdown
- **File:** `placeholder-recipe.jpg`
- **Source URL:** https://www.freepik.com/free-photo/...
- **License:** Freepik Free License
- **Author:** photographer_name
```

### 4. Optimize Downloaded Images

Use ImageOptim, TinyPNG, or similar tools to:
1. Resize to 1200x800px (if larger)
2. Compress to ~150KB
3. Convert AVIF to JPG if needed

### Existing Images

These 4 images already exist and should be added to ATTRIBUTION.md with their sources:
- `caesar-salad-with-shrimp-prawn_74190-952.jpg` (260KB)
- `high-angle-tasty-truffle-recipe_23-2149525124.jpg` (280KB)
- `stir-fry-chicken-sweet-peppers-green-beans_2829-20113.avif` (178KB)
- `turkish-street-food-lahmacun-with-lemon-fresh-parsley-melted-cheese-top_114579-4348.jpg` (955KB)

## Next Steps: Phase 2 & 3 (Image Upload Feature)

After completing the image downloads, we can proceed with:

**Phase 2: Backend Setup**
- Create Supabase Storage bucket for user uploads
- Add storage helper functions
- Update recipes edge function to accept image uploads

**Phase 3: Frontend UI**
- Add image upload to recipe creation form
- Add preview and validation
- Implement image processing utilities

## Verification

After downloading the placeholder image, verify:
1. Navigate to http://localhost:3000/recipes
2. Recipe cards should show images (not broken)
3. Recipes without image_url show the placeholder
4. Images have hover effects (scale on hover)

## Quick Start (Minimum Setup)

To get the app working immediately:
```bash
# Create placeholder from existing image
cd "/Volumes/Untitled/Projects/AIMakeFood/web-app/public/images/recipes/"
cp "high-angle-tasty-truffle-recipe_23-2149525124.jpg" "placeholder-recipe.jpg"
```

Then reload the app - images should display correctly!
