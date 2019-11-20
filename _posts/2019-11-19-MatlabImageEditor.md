---
title: "Image Combiner and Remover"
date: 2018-11-19
tags: [image editing, vectorisation, matLab]
header:
excerpt: "Image Combiner and Remover using matLab"
---

## Project Outline

This image combiner and remover was my project as part of my first year engineering paper ENGGEN 131.

An example of its functions can be seen in the images below with the following set of 4 images:

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Overview.JPG" alt="">


Image Combiner

The image combiner script that I wrote combines each of the images in order to create an - action shot, as seen below with the image:

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Action Shot.JPG" alt="">


Image Remover

The image remover script on the other hand does the opposite - it uses the three images in order to remove the objects from the images to create a image removed image:

<img src="{{ site.url }}{{ site.baseurl }}/images/matlab/Remove Action.JPG" alt="">


## Image Editing Mechanics

The image remover works by finding the median value of each of the RGB layers in each of the pixels between the images provided. This median value is then stored in a new cell array which then becomes the new image. As the **median filter** is applied to every RGB pixel in the image, the resulting is a pixel that will contain the most common pixel - the one of the background instead of the moon in this case, taking the moon out of the images in the output image.

The median filter can be seen here:

```matlab
    function[med_r, med_g, med_b] = MedianPixel(colour_matrix)
    % take the median of each layer - r, g, b
    med_r = median(colour_matrix(:, :, 1));
    med_g = median(colour_matrix(:, :, 2));
    med_b = median(colour_matrix(:, :, 3));
```

The code for remove action is shown here:

```matlab
function[Removed_Action] = RemoveAction(image_array)
% find dimensions of image
[rows, columns, layer] = size(image_array{1});

% for every pixel in the image
for r = 1:rows
    for c = 1:columns
        % for every R, G and B pixel in each photo find the median
        for i = 1:length(image_array)
            r_pixel(i) = image_array{i}(r, c, 1);
            g_pixel(i) = image_array{i}(r, c, 2);
            b_pixel(i) = image_array{i}(r, c, 3);
        end

        % convert RGB input into correct format
        rgb_input(:,:,1) = r_pixel;
        rgb_input(:,:,2) = g_pixel;
        rgb_input(:,:,3) = b_pixel;
        % find median of these values
        [r_med, g_med, b_med] = MedianPixel(rgb_input);

    end
end
```

Similarly with the image combiner, instead of just a median filter being applied and then added to a cell array which is the output image, the pixel that is furthest in value from the median value is the value that is stored in the cell array for the output. Between four images, this means that the pixels that are the most different - the ones that contain the moon will be the ones that are stored. This allows for the moon to be captured from each of the images.

The code for the action shot is below, where the MostDistantPixel function finds the most distant pixel as explained previously:

```matlab
function[Action_Shot] = ActionShot(image_array)
% find dimensions of image
[rows, columns, layers] = size(image_array{1});

% for every pixel in the image
for r = 1:rows
    for c = 1:columns
        % for every RGB pixel in each photo apply MostDistantPixel function
        for i = 1:length(image_array)
            r_pixel(i) = image_array{i}(r, c, 1);
            g_pixel(i) = image_array{i}(r, c, 2);
            b_pixel(i) = image_array{i}(r, c, 3);
        end

        % convert RGB input into correct format
        rgb_input(:,:,1) = r_pixel;
        rgb_input(:,:,2) = g_pixel;
        rgb_input(:,:,3) = b_pixel;
        % find most distant pixel of these RGB values
        [mostd_r, mostd_g, mostd_b] = MostDistantPixel(rgb_input);

        % store pixels in new array
        Action_Shot(r, c, 1) = mostd_r;
        Action_Shot(r, c, 2) = mostd_g;
        Action_Shot(r, c, 3) = mostd_b;
    end
end

```

The code for the action shot is basically the same as the remove action but with added steps of finding the most distant pixel from the median pixel value.
