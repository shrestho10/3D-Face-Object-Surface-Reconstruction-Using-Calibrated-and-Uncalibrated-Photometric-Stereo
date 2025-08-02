main code has to be downloaded from:
https://github.com/guanyingc/SDPS-Net.git

Then the only change made was to get the predicted normal, so the file were changed in the repository is:

test_stage2.py and the function I changed was the following:


def prepareSave(args, data, pred_c, pred,i):
    results = [data['img'].data, data['m'].data, (data['n'].data+1) / 2]
    if args.s2_est_n:
        masked_pred2 = pred['n'] * data['m'].data.expand_as(pred['n'].data)
        save_raw_normal(masked_pred2, f"./shagoto_predicted_normal/normal_shagoto{i}.npy")
        pred_n = (pred['n'].data + 1) / 2
        masked_pred = pred_n * data['m'].data.expand_as(pred['n'].data)
        res_n = [masked_pred, data['error_map']]
        results += res_n
        #save_raw_normal(masked_pred, f"./shagoto_predicted_normal/normal_shagoto{i}.npy")

    nrow = data['img'].shape[0]
    return results, nrow


