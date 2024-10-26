from pathlib import Path

# Create the folder structure based on the previous design
base_path = Path("/mnt/data/Master Assets")

# Define main folders and their subfolders
folder_structure = {
    "Core Elements": ["Branding Kit"],
    "Content Library": ["Editorial Bank"],
    "Design Patterns": ["Component Reuse"],
    "Media Vault": ["Audio & Music"],
    "Interaction Prototypes": ["Animation"],
    "Project Blueprints": ["Strategic Goals"]
}

# Create main folders and subfolders
for main_folder, subfolders in folder_structure.items():
    main_folder_path = base_path / main_folder
    main_folder_path.mkdir(parents=True, exist_ok=True)
    for subfolder in subfolders:
        (main_folder_path / subfolder).mkdir(parents=True, exist_ok=True)

# Display the created structure
sorted(list(base_path.glob("**/")))