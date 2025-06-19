# Public Image Uploader for GitHub

This project allows you to upload images to a GitHub repository and automatically organize them into folders by year (2025), month, and day. PNG and JPG images are automatically converted to WEBP format for better optimization. Each uploaded image will have a public link that can be used anywhere on the web.

## Features
- Automatically uploads images to your GitHub repository
- Organizes images into folders: `2025/<month>/<day>/`
- Converts PNG, JPG, JPEG images to WEBP format before uploading
- Generates a public URL for each image

## Requirements
- Python 3.7+
- [requests](https://pypi.org/project/requests/)
- [Pillow](https://pypi.org/project/Pillow/)

Install dependencies:
```bash
pip install requests pillow
```

## Setup
1. **Create a public GitHub repository** (e.g., `public-images`).
2. **Generate a GitHub Personal Access Token** with `repo` scope: [Create Token](https://github.com/settings/tokens)
3. **Edit `uoload_image.py`**:
   - Set your GitHub username, repository name, and token at the top of the script:
     ```python
     GITHUB_USER = "YourGitHubUsername"
     GITHUB_REPO = "public-images"
     GITHUB_TOKEN = "YOUR_GITHUB_TOKEN"
     ```

## Usage
1. Run the script:
   ```bash
   python uoload_image.py
   ```
2. Enter the path to your image file (e.g., `C:\Users\YourName\Pictures\myphoto.jpg`).
3. The script will:
   - Convert the image to WEBP if it is PNG/JPG/JPEG
   - Upload it to your GitHub repo under `2025/<month>/<day>/`
   - Print out the public URL for the image

## Example
```
Nhập đường dẫn file ảnh: C:\Users\YourName\Pictures\myphoto.jpg
Upload thành công!
Link public: https://raw.githubusercontent.com/YourGitHubUsername/public-images/main/2025/06/01/myphoto.webp
```

## Notes
- If the file already exists in the same folder, the script will notify you.
- You can use the public link anywhere (HTML, Markdown, etc.).

---

**Happy sharing your images!**
