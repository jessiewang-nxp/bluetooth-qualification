The \images folder in the Obex File System directory is intended for use with BIP.  The information stored in this folder will be used when the tester is acting as the server, and a client is requesting image information.

Each image will have its own folder, with the same name as the image hanlde.  For example:
ImgHandle = 00000001, The folder \images\00000001, will contain all the image information associated with that image handle.  Inside the folder the following files may exist
* x-bt\img-properties (an extensionless file in the x-bt folder).  This contains valid XML per the img-properties for this image as defined in BIP.
* x-bt\img-img (an extensionless file in the x-bt folder).  This file contains the native variation of the image
* x-bt\img-img.$encoding.$pixelwidth.$pixelheight (a sort of extensionless file in the x-bt folder).  This file contains the variant with the encoding,pixelwidth and pixelheight as described in the img properties.
* x-bt\img-thm (an extensionless file in the x-bt folder).  This file contains the linked thumbnail image.  There must be a duplicate file for x-bt\img-img (if its the native format no extension is needed, otherwise it needs the variant extension)
