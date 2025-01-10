#pseudocode for detecting objects and sub-objects

FUNCTION detect_objects(video_source):
    results_list = []

    FOR each frame in video_source:
        detections = detect objects in frame
        
        FOR each detection in detections:
            object_name = detection's name
            object_id = get unique ID
            bbox = detection's bounding box
            
            IF detection has subobjects:
                subobject = detection's first subobject
                sub_id = get unique ID
                ADD {
                    "object": object_name,
                    "id": object_id,
                    "bbox": bbox,
                    "subobject": {
                        "object": subobject's name,
                        "id": sub_id,
                        "bbox": subobject's bounding box
                    }
                } to results_list
            ELSE:
                ADD {
                    "object": object_name,
                    "id": object_id,
                    "bbox": bbox,
                    "subobject": null
                } to results_list

    RETURN results_list






   # pseudocode for formatting detection results to JSON

   FUNCTION format_to_json(detection_results):
    json_output = []

    FOR each result in detection_results:
        item = {
            "object": result's object,
            "id": result's id,
            "bbox": result's bbox
        }
        
        IF result has subobject:
            item["subobject"] = {
                "object": result's subobject's object,
                "id": result's subobject's id,
                "bbox": result's subobject's bbox
            }
        ELSE:
            item["subobject"] = null
        
        ADD item to json_output

    RETURN convert json_output to JSON format


# pseudocode for adding a new object-subobject pair



FUNCTION add_new_object_subobject_pair(object_name, subobject_name):
    CALL object_detector to add object with name object_name
    CALL object_detector to add subobject with name subobject_name to object_name
    
    PRINT "Added relationship: " + object_name + " -> " + subobject_name


