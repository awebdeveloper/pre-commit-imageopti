Pre-commit hook for Imageoptim-cli on Mac  
==========================================

This is a imageoptim-cli hook for [pre-commit](https://github.com/pre-commit/pre-commit). This optimised images on commit.


### Using imageoptim with pre-commit

- To use this you first need to install pre-commit(see links below).
- Then create a pre-commit config file.
- Run `pre-commit install` from the root of your project
- Download ImageOptim for Mac.
- Additionally download ImageAlpha and JPEGmini for Mac

Finally add this to your `.pre-commit-config.yaml`:

```yaml
   -   repo: https://github.com/awebdeveloper/pre-commit-imageoptim
       rev: '' # Use the sha or tag you want to point at like 0.0.1
       hooks:
       -   id: imageoptim
           additional_dependencies: ['imageoptim-cli']
 ```
PS: These are for version 2.3.0 visit https://pre-commit.com/#2-add-a-pre-commit-configuration for latest config syntax or for config syntax specific to your version

 Now everytime you commit a png/jpg file. It will run imageoptim-cli on this and optimise the file.

### FAQ's

  **1.** Why does pre-commit say failed everytime the images are changed by the file.

  **A.** This is how pre-commit works. You need to just add the files again and commit. This is done so that you can verify the changes.

  **2.** Why only mac.

  **A.** Imageoptim is only on mac, if and when it does add other platform we will support it.
  
  
  **3.** How to pass Pass extra args
  
  **A.** Read precommit docs on how to use args property.
  

 ### Links
 - For pre-commit: see https://github.com/pre-commit/pre-commit
 - For ImageOptim-CLI: see https://github.com/JamieMason/ImageOptim-CLI/


