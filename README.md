# Envcanlib
Python3 package to download information from Environment Canada: Whether Information

## Description

**envcanlib.downloadData**(IDs, start, end, method='hourly', path='', dataFormat='default', continuous=True,
metaData=None)

    Pull daily or hourly information from the Government of Canada official website of a specified period of time and save the data in the disk.

    Parameters:

        IDs : list of strings, array_like as str type

            List of staions  IDs.

        start : tuple as int type
            
            A tuple containing year and month to start.
        
        end : tuple as int type
            
            A tuple containing year and month to end.

        method : string, optional
            
            'hourly' for hourly information and 'daily' for daily information.

        path : string, optional
            
            Path to save the data in the disk. The default directory is the root directory.

        dataFormat: string, optional

            'default' means that it will be saved one file for each ID in IDs. 'oneFile' means that
            one file containing all pulled information will be saved.

        continuous: bool, optional

            If True all information between start and end will be pulled, otherwise it will be pulled just the information between start month and end month from start year until end year. 
            For instance, if start = (2014,5) and end = (2015,7) and continuous = False, then it will be pulled just the months 5,6 and 7 of 2014 and 2015. If continuous = True, all the data between March 2014 and July 2015 will be pulled. 
            This can be useful if it is desired to have slices of a period of time.

        metaData: pandas.DataFrame, optional

            In case dataFormat is passed as 'oneFile' this dataframe will be used to get more information about the stations. This parameter is always optional.

    Returns:

        None.

## Dependencies

- Numpy
- Urllib
- Pandas