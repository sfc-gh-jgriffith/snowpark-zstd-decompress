# Using Snowpark to implement ZSTD dictionary decompression
Snowflake has compress and decompress function that support ZSTD, but it does not support a user-supplied dictionary file. This code demonstrates:
1. Connecting to Snowflake using the Snowpark for Python connector.
2. Creating fake data using the Faker library and creating a ZSTD dictionary file. 
3. Uploading that faked & compressed to a Snowflake table.
4. Upload our dictionary file to a stage and create a Python UDF to decompress data using that file.
5. Calling that Python UDF using ordinary SQL
