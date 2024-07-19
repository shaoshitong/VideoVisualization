### Accelerated Sampling in Video Stable Diffusion

Our method need 16 iterations for finishing the total pipeline. Now I find that even in the 6th iteration the model seem to be surprisingly well!

**Definition: For example, Iter=3 refers to the 3rd iteration**

<table style="width: 100%; border-collapse: collapse; font-family: Arial, sans-serif; font-size: 14px; text-align: center;">
        <thead style="background-color: #f2f2f2; border-bottom: 2px solid #ddd;">
            <tr>
                <th style="padding: 10px;">Baseline</th>
                <th style="padding: 10px;">Iter=3</th>
                <th style="padding: 10px;">Iter=6</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><img src="./src2/0-data-cache-vanilla-step2.gif" alt="Recall = 0" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/0-data-cache-iter3-step2.gif" alt="Recall = 1" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/0-data-cache-iter6-step2.gif" alt="Recall = 2" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
            </tr>
            <tr style="border-bottom: 1px solid #ddd;">
                <td style="padding: 2px 10px;">Step=2, "A dog walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=2, "A dog walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=2, "A dog walking on a treadmill"</td>
            </tr>
            <tr>
                <td><img src="./src2/0-data-cache-vanilla-step4.gif" alt="Recall = 0" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/0-data-cache-iter3-step4.gif" alt="Recall = 1" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/0-data-cache-iter6-step4.gif" alt="Recall = 2" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
            </tr>
            <tr style="border-bottom: 1px solid #ddd;">
                <td style="padding: 2px 10px;">Step=4, "A dog walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=4, "A dog walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=4, "A dog walking on a treadmill"</td>
            </tr>
            <tr>
                <td><img src="./src2/0-data-cache-vanilla-step8.gif" alt="Recall = 0" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/0-data-cache-iter3-step8.gif" alt="Recall = 1" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/0-data-cache-iter6-step8.gif" alt="Recall = 2" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
            </tr>
            <tr style="border-bottom: 1px solid #ddd;">
                <td style="padding: 2px 10px;">Step=8, "A dog walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=8, "A dog walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=8, "A dog walking on a treadmill"</td>
            </tr>
            <tr>
                <td><img src="./src2/1-data-cache-vanilla-step2.gif" alt="Recall = 0" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/1-data-cache-iter3-step2.gif" alt="Recall = 1" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/1-data-cache-iter6-step2.gif" alt="Recall = 2" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
            </tr>
            <tr style="border-bottom: 1px solid #ddd;">
                <td style="padding: 2px 10px;">Step=2, "A cat walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=2, "A cat walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=2, "A cat walking on a treadmill"</td>
            </tr>
            <tr>
                <td><img src="./src2/1-data-cache-vanilla-step4.gif" alt="Recall = 0" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/1-data-cache-iter3-step4.gif" alt="Recall = 1" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/1-data-cache-iter6-step4.gif" alt="Recall = 2" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
            </tr>
            <tr style="border-bottom: 1px solid #ddd;">
                <td style="padding: 2px 10px;">Step=4, "A cat walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=4, "A cat walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=4, "A cat walking on a treadmill"</td>
            </tr>
            <tr>
                <td><img src="./src2/1-data-cache-vanilla-step8.gif" alt="Recall = 0" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/1-data-cache-iter3-step8.gif" alt="Recall = 1" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
                <td><img src="./src2/1-data-cache-iter6-step8.gif" alt="Recall = 2" style="width: 235px; height: 235px; padding: 5px 10px;"></td>
            </tr>
            <tr style="border-bottom: 1px solid #ddd;">
                <td style="padding: 2px 10px;">Step=8, "A cat walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=8, "A cat walking on a treadmill"</td>
                <td style="padding: 2px 10px;">Step=8, "A cat walking on a treadmill"</td>
            </tr>
   </tbody>
</table>    