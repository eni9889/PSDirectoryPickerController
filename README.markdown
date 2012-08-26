#Sample use
    PSDirectoryPickerController *directoryPicker = [[PSDirectoryPickerController alloc] initWithRootDirectory:@"/path/to/some/directory/"];
    
    [directoryPicker setDelegate:self];
    [directoryPicker setPrompt:@"Choose a directory"];
    [directoryPicker setModalPresentationStyle:UIModalPresentationFormSheet];
    
    [self presentModalViewController:directoryPicker animated:YES];

---

    - (void)directoryPickerControllerDidCancel:(PSDirectoryPickerController *)picker
    {
    	NSLog(@"Cancelled!");
	}

	- (void)directoryPickerController:(PSDirectoryPickerController *)picker didFinishPickingDirectoryAtPath:(NSString *)path
	{
	    NSLog(@"Picked directory at %@", path);
	}