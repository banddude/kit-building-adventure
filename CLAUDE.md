# Complete Workflow: From Photo Export to GitHub Story Repository

## Phase 1: Photo Export and Setup
1. **Export photos from Kit album**
   ```
   Use: mcp__aiva__photos_export_kit_pics
   Parameters: count=5, destination=~/Desktop/kit-pics
   ```

2. **Navigate to the exported folder**
   ```bash
   cd ~/Desktop/kit-pics
   ls -la  # Verify photos exported correctly
   ```

## Phase 2: Location Analysis
3. **Extract location metadata from all photos**
   ```bash
   mdls -name kMDItemLatitude -name kMDItemLongitude -name kMDItemContentCreationDate -name kMDItemDisplayName *.jpeg
   ```

4. **Look up each unique location using maps**
   ```
   Use: mcp__aiva__maps_search for each coordinate pair
   Document the addresses found
   ```

5. **Search memory for relevant context**
   ```
   Use: mcp__aiva__search_memories with location keywords
   Find connections to Mike's life/work/home
   ```

6. **Create location notes document**
   - List each photo with its location
   - Note the progression/story timeline
   - Identify what each location represents

## Phase 3: Image Analysis and Story Planning
7. **View each image individually**
   ```
   Use: Read tool on each IMG_*.jpeg file
   Take detailed notes on:
   - What Kit is doing
   - What Mike is doing  
   - Setting/environment details
   - Expressions and mood
   - Objects and activities visible
   ```

8. **Create story outline**
   - Map photos to story chapters
   - Identify narrative arc
   - Plan chapter titles and progression
   - Note which photo illustrates each chapter

## Phase 4: Story Creation
9. **Write the complete story**
   ```
   Use: Write tool to create README.md
   Include:
   - Chapter-based structure
   - Embedded images with proper paths
   - Location context woven into narrative
   - Fun, engaging tone
   - Technical details about the workflow
   ```

## Phase 5: Repository Creation and Publishing
10. **Initialize new git repository**
    ```bash
    git init
    git add .
    git commit -m "Initial commit: [Story Title] with photos"
    ```

11. **Create GitHub repository**
    ```bash
    gh repo create [repo-name] --public --description "[Story description]" --source=.
    ```

12. **Push to GitHub**
    ```bash
    git push -u origin main
    ```

13. **Open the final repository**
    ```bash
    open https://github.com/banddude/[repo-name]
    ```

## Phase 6: Quality Assurance
14. **Verify the final product**
    - Check that all images display correctly
    - Verify story narrative flows well
    - Confirm location context is accurate
    - Test all markdown formatting

## Additional Steps (if needed):
- **Update story with location context** if discovered after initial writing
- **Commit and push updates** with descriptive commit messages
- **Use TodoWrite tool** to track progress through complex workflows
- **Test with curl/verification** if technical integrations are involved

This workflow transforms a simple photo export into a complete, contextualized story repository with proper version control and public sharing.