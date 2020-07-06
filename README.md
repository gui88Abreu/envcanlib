# envcanlib
Python package to download information from Environment Canada: Whether Information


## Description

**envcanlib.downloadData**(IDs, start, end, method='hourly', path='', dataFormat='default', continuous=True,
metaData=None)

    Pull daily or hourly information from the Government of Canada official website of a specified period of time and store the data in the machine.

    Parameters:

        IDs : list of strings, array_like as type str

            List of IDs.

        start : tuple as type int
            
            A tuple containing year and month to start.
        
        end : tuple as type int
            
            A tuple containing year and month to end.

        method : string, optional
            
            'hourly' for hourly information and 'daily' for daily information.

        path : string, optional
            
            Path to be stored the data in the machine. The default directory is the root directory.

        dataFormat: string, optional

            'default' means that it will be stored one file for each ID in IDs. 'oneFile' means that
            one file containing all pulled information will be stored.

        continuous: bool, optional

            If True all information between start and end will be pulled, otherwise it will be pulled just the information between start month and end month since start year until end year.

        metaData: pandas.DataFrame, optional

            In case dataFormat is passed as 'oneFile' this dataframe will be used to get more information about the stations. This parameter is always optional.

    Returns:

        None.
