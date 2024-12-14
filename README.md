# Read Me

A test repo to mirror the way that Trac works using Labels in GitHub with GitHub Actions

## Issue Templates

There are 3 issue templates that are driven by the base template. This allows a user to select the issue type when
creating the issue AND it keeps the contents syncronized. If you need to make a change to an issue template (for example 
to add a new version of Django) you would update the `base.yml` and a GHA will update the `bug.yml`, `cleanup.yml` and
`feature.yml` automatically

Labels will be added to the issue based on the data that is selected by the reported, i.e. Easy Pickings, Has Patch,
etc. The issue description will be cleaned up though to ONLY include what is entered into the Description field of
the template

## Assigning Issues

There are 2 assignment commands:

- `/take` - will make you the sole assignee of an issue
- `/assign` - will add you to the current list of assignees

There is a GHA that will remove these comments though to keep the comment history clean

## Updating Labels

There are 3 label commands

- `/label` - adding a comment of `/label bug` will add the label of `bug`
- `/remove-label` - adding a comment of `/remove-label bug` will remove the 
label of `bug`
- `/labels` 0 adding a comment of `/labels` will list all available labels

Currently you can only add or remove one label at a time