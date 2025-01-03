### Add files

# Initialize LFS

git lfs install

# Set up tracking

git lfs track "data/\*\_mainnet.json"
git add .gitattributes

# Remove files from regular git tracking if they're already tracked

git rm --cached "data/\*\_mainnet.json"

# Add the files to LFS

git add "data/\*\_mainnet.json"

# Verify they're being tracked by LFS

git lfs ls-files

# Commit

git commit -m "Add files to LFS"

# Push LFS objects first

git lfs push origin master --all

# Then push the commit

git push origin master
