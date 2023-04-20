
    
For training, run: ``python3 scripts/segmentation_train.py --data_name ISIC --data_dir ~/MedSegDiff-oct/data/goals --out_dir ~/MedSegDiff-oct/output --image_size 256 --num_channels 128 --class_cond False --num_res_blocks 2 --num_heads 1 --learn_sigma True --use_scale_shift_norm False --attention_resolutions 16 --diffusion_steps 1000 --noise_schedule linear --rescale_learned_sigmas False --rescale_timesteps False --lr 1e-4 --batch_size 2``
    
For sampling, run: ``python3 scripts/segmentation_sample.py --data_name ISIC --data_dir ~/MedSegDiff-oct/data/goals --out_dir ~/MedSegDiff-oct/res --model_path ~/MedSegDiff-oct/output/xx.pt --image_size 256 --num_channels 128 --class_cond False --num_res_blocks 2 --num_heads 1 --learn_sigma True --use_scale_shift_norm False --attention_resolutions 16 --diffusion_steps 1000 --noise_schedule linear --rescale_learned_sigmas False --rescale_timesteps False --num_ensemble 5``

For evaluation, run ``python scripts/segmentation_env.py --inp_pth *folder you save prediction images* --out_pth *folder you save ground truth images*``