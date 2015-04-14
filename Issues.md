#  Issues List

This represents a list of issues that needs to be discussed on the mailing list to make decisions about the document.  This list will be updated as items are sent to the list and decisions are made.

#  General Issues

1.  Switch to using arrays for some maps.  Issues includes which maps are to be changed and if null types or absent values are to be used.

2.  Create new top level type for MAC

3.  CBOR encodings - use binary not base64 - criteria of decisions and indication of which is used

4.  Use CBOR encoding for building octet strings to be cryptographically processed.

4.  Indicator for which type of message we are looking at - Use integer or tagging?  This includes a question of registering for CBOR tagging of each type or just the top level type as well.  Do we even create a top level CBOR message type or group?  It would be useful for including in other specifications.


6.  Mapping of strings to integers:  Is this global to both tags and values or just for tags?  Do we need to have a policy for having assignment ranges (tags, values, private use)?  Is this a single table or is it spread over multiple registries?  IANA considerations for updating the table?

1.  Compression:  Do we keep it as is, remove it as being not useful, create a new message type just for compression?

1.  Strict Mode encoding:  Do we only allow for strict on everything for just on some things?  Possible sub issue here is do we keep the binary wrapping on all of the maps or not?  There is a possibility to say re-encode canonically.

1.  Flattened encoding:  Is there a need to do a flattened encoding or should it be eliminated?

#  Signed Message Issues

1.  Separation of attributes into message and signature attributes.  Problem if one wants to add message attributes to an existing message.  Cleaner in terms of what gets duplicated.

#  Encrypted Message Issues

1.  Make Key Management more uniform:  This includes two different issues.  1) use a single structure for all of the different key management structures including direct by making a separation of layers.  2) Use the same structure as the base message.

2.  Roll authentication tag into encrypted value

3.  Deal with authenticated data that is in the message and authenticated data that is parallel to the message.  (i.e. outer message headers)

4.  Add authenticated data to the recipient layer.

5.  Key Management section:  Needs review of all of the requirements on presence and for readability.

#  MAC Message Issues

1.  Adding in key management

2.  IANA considerations to add mac operations to the current key_ops field.

# Algorithm Issues

1.  Are we allowing all of the JOSE algorithms across or are we going to deprecate some of them.

2.  Define a key wrap mode (AES-GCM or CCM) to allow for authenticated attributes at the wrapping level.

# Attribute specific issues

1.  Should kid be a binary rather than a text value?

5.  Dealing with COSE keys. Sub items are: 1) define a new tag for this when used in structures.   2) IANA registrations of mime media types.

1.  Presence requirements:  Need to do a general review of what fields MUST and SHOULD be present in different messages.

