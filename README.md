# NVBlink-Peertube-NVIDIA-Transcoding
Finally, a Peertube Plugin that allows for true, FULL Nvidia Hardware Acceleration for transcoding, offering both decoding and encoding using Nvidia GPUs for hardware acceleration. Written for legacy GPUs, guaranteed to be compatible with M10, P4, and newer graphics cards. Supports multiple GPUs simultaneously, distributing jobs between each gpu. 

From within the Peertube plugin UI, enter the number of GPUs you have at your disposal to use for full hardware transcoding, hit save, and monitor on your server using a tool like nvidia-smi or my favorite nvtop. Each job will be assigned to a single gpu, and each subsequent job will be assigned to another gpu, and so on, until jobs are evenly distributed amongst the number of gpus given on the plugin's settings page. 

If you experience issues setting the number of GPUs, first, check the peertube systemd service file, and make sure that security settings aren't preventing the process from accessing your hardware in the first place. Further, after setting the number of GPUs, restart the peertube service if you experience issues with all gpus being used. 

Feel free to open any issues or just provide feedback here on github or shoot me an email at themadhacker@themadhacker.net

