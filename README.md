# Git LFS

This workshop is on [Git LFS (Large File Storage)](https://git-lfs.github.com/),
which versions data, images, fonts, PDFs, etc. efficiently in Git.
It's best for large non-text files.

This assumes you're familiar with [Git](https://git-scm.com/).

[See video tutorial](https://youtu.be/uLR1RNqJ1Mw)

## Git LFS quick start

These commands set up a repository to track JPG and PNG files with Git LFS:

```bash
# Set up Git LFS. You only need to run this once per user account
git lfs install

# Use Git LFS to manage all .jpg and .png files
git lfs track "*.jpg" "*.png"

# Use Git LFS to manage all files under `assets/`
git lfs track "assets/**"

# Track .gitattributes for others who clone the repo to use Git LFS
git add .gitattributes
git commit -m"Add Git LFS for images"
git push
```

## Setup

1. [Install Git](https://git-scm.com/)
2. [Install Git LFS](https://git-lfs.github.com/)

## Exercise

1. [Fork this repo](https://code.gramener.com/cto/git-lfs-workshop/-/forks/new) into your namespace. Use `git` to clone your fork
2. Run `git lfs install` to set up Git LFS for your account
3. Save [this image](https://web.archive.org/web/20220526174227im_/https://upload.wikimedia.org/wikipedia/commons/thumb/2/21/Mandel_zoom_00_mandelbrot_set.jpg/322px-Mandel_zoom_00_mandelbrot_set.jpg) as `img/small.jpg` (use this **EXACT** path)
4. Save [this PDF file](https://arxiv.org/pdf/math/9711213) as `docs/9711213.pdf` (use this **EXACT** path)
5. Unzip the [Joan font](https://fonts.google.com/download?family=Joan) font under `fonts/` (use this **EXACT** path)
6. Track all `*.jpg`, `*.png` and `*.pdf` files with Git LFS
7. Track all files under `fonts/` with Git LFS
8. Add all files (including `.gitattributes`) using `git add .`
9. List all tracked files by typing `git lfs ls-files > lfs-files.txt`. This saves the list of LFS files as `lfs-files.txt` in the root of your repository (use this **EXACT** path)
10. Add `lfs-files.txt`, commit and push the code to your fork
11. [Create an issue][issue] titled `Exercise submission`. Add a link to your repo and submit the issue.

[issue]: https://code.gramener.com/cto/git-lfs-workshop/-/issues/new?issue[title]=Exercise+submission&issue[description]=Link+to+my+repo:+
