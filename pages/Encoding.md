- Every CVM Data Object has an Encoding, which is a representation of the Object as a sequence of bytes.
  
  Encodings are designed to be:
- Small in size (to minimise storage and network bandwidth requirements)
- Efficient for serialisation and deserialisation
- Canonical (i.e. any Data Object has one and only one valid Encoding)
  
  The maximum Encoding size is 8191 byes. Larger Data Objects are broken down into multiple Cells which each have their individual Encoding - however this is handled automatically by Convex and not usually a relevant concern for users or developers.