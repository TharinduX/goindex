# GoIndex

This is a [modified version of goindex](https://github.com/yanzai/goindex) ，In [original goindex](https://github.com/donwa/goindex) Multi-disk support, search, paging loading and other functions have been added.

`index.js` contains the code needed by Workers.

## Preview

Demo: https://yanzai-goindex.java.workers.dev

Multiple disks:
![Multi-disc](imgs/1.png)

search for:  
![Search](imgs/2.png)

Pagination:
![Pagination](imgs/3.png)


## Update log

### 2020-4-28

- Add Basic Auth authentication, user name and password can be configured separately for each drive letter, can protect all sub files and sub folders under the drive

- Support custom web interface theme color, add dark_mode; can be configured in `uiConfig`

- The original .password verification method of goindex is retained as a backup verification method, but it is not enabled by default.

  For details, please refer to the notes of the configuration items in `index.js`.

### 2020-4-23

- Support calling nPlayer / MXPlayer Free / MXPlayer Pro / PotPlayer / VLC player, support direct copy straight chain
- Simple support for PDF file preview
- Can configure whether to allow other web front-end cors to obtain files

### 2020-3-9

- flac file play support

### 2020-3-7

- Add search function, incremental display of search results, and support jump to the corresponding path to browse
- Search function supports full search for personal and team
- The search pagination size can be configured, see the `index.js` note
- Try to solve the problem of incremental loading when the mobile terminal scrolls to the bottom
- UI optimization, drive letter selection changed to drop-down box display

### 2020-3-5

- Pagination incremental loading of file list page, support custom paging size, multi-page content can be cached, see `index.js` configuration
- Picture browsing page Next / Previous Navigation
- Optimized speed when listing directories

### 2020-3-4

Modify on the basis of the original version:

- Add multi-disk support, set the multi-disk to be displayed and their passwords independently
- Only the material is modified on the front end, so classic theme is not supported
- See `index.js` comments for configuration
  

---



> ** You can refer to the original version for installation and deployment. The following is taken from the deployment instructions of the original version of goindex: **


## Demo  
not working anymore

## Deployment  
1.Install `rclone` software locally  
2.Follow [https://rclone.org/drive/]( https://rclone.org/drive/) bind a drive  
3.Execute the command`rclone config file` to find the file `rclone.conf` path  
4.Open `rclone.conf`,find the configuration `root_folder_id` and `refresh_token`  
5.Download index.js in https://github.com/donwa/goindex and fill in root and refresh_token  
6.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)

## Quick Deployment  
1.Open https://installen.gd.workers.dev/  
2.Auth and get the code  
3.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)  

## About  
Cloudflare Workers allow you to write JavaScript which runs on all of Cloudflare's 150+ global data centers.  
