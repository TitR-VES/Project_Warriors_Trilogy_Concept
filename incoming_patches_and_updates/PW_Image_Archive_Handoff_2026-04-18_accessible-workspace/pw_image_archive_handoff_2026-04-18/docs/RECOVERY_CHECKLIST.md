# Manual Recovery Checklist

Use this checklist while downloading images from prior ChatGPT project chats.

## Export procedure

1. Open the relevant Project Warriors chat.
2. Locate each generated image output.
3. Open/download the image from the ChatGPT UI.
4. Save it using the suggested filename style.
5. Place it in the matching repository folder.
6. Update `manifests/generated_image_manifest.csv`:
   - set `binary_status` to `exported`
   - fill in `repo_path`
   - add `notes` if the image has text-overlay errors, wrong insignia, drift, or should be used only as a loose reference

## Priority order

1. Character reference images used for identity consistency.
2. Accepted promo stills.
3. Patch/logo boards.
4. Civilian memory/tourist photos.
5. Brand/environment exploration boards.

## Quality-control flags to preserve

- Halliday images with generated overlay text should be kept, but overlay text should be corrected manually or omitted/reapplied in post.
- Switchblade Kaliningrad harbor image should prefer the revised cover/concealment logic where she is clearly not standing exposed in the helicopter line of sight.
- Frost visual work is still flagged for future development and should not be treated as complete unless the full unmasked/scarring reference package has been produced.
- User-uploaded reference images should be separated from assistant-generated preview images so collaborators can tell source reference from generated output.
