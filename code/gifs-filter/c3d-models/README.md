
== For c3d models ==
* train.py: train c3d-models
    * data format: a directory with
        * c3d.list, c3d.npy (generated by ./c3d/c3d.sh)
* predict.py: filter based on c3d-models

== models ==

* ./giftype/c3d-models-rfc.pkl: the model trained on giftypes, which removes the static animated GIFs and the cartoon GIFs.
* ./no-motion/c3d-models-rfc.pkl: the model trained on a dataset with 1400 GIFs to remove no enough motion GIFs

== utility ==
* setdiff.py: A - B
* setinter.py: A & B

== For other pipelines ==
They are here for dependency on functions defined in train.py and predict.py

* filter-images.py: filter url path list based on url list
    * no_rm: we allow for multiple url path matching the same url
* cluster-by-tags.py: given tags of images, cluster based on kmeans
* dump-tags.py: dump autotags output to raw text format
* filter_tags.py: filter GIFs based on autotags
    * tag_rules to define urls over the autotags
* filter-text.py: filter based on text score of the frames