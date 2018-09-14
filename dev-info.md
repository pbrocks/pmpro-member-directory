# PMPro Member Directory

Context: PMPro Member Directory .5.1 checks either the active theme directory or its own folders for the template files. The folders are also named differently. Paths are set in base file. In addition, there is a global $pmpromd_options that is unused.

## pmpro-member-directory .5.2
- Added 3 functions to fire on `init` with an overt priority of `10`
 - `pmpromd_define_paths` creates 4 paths and stores them in the global variable.
   - path to the profile and directory files that ship with the Add On
   - path to the active theme's folders
   - path to the PMPro Customizations plugin
   - custom path as defined by a filter, with the Customizations plugin path as the default backup
 - `pmpromd_get_profile_file` checks each path to see if a `profile.php` exists and selects the last one it finds.
 - `pmpromd_get_directory_file` checks each path to see if a `directory.php` exists and selects the last one it finds.

### [Inspiration Thread](https://www.paidmembershipspro.com/forums/topic/filter-members-by-register-helper-select-field/#post-163219)