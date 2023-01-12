IMP: USE ipykernel as venv. Plotly errors out in pip venv

initialize-
script_data = ScriptData()
startegy_scriptname = Strategy(script_name)



class ScriptData:
methods:
    get_intraday_data(script_name) - gets data with requests lib and stores in dictionary as {"script_name": data}
    
    convert_intraday_data(script_name) - if script in that dictionary then creates dataframe of that script.
    
    __getitem__(script_name) - gets dataframe of script if script in dictionary.   


    __contains__(script_name) - check if script is in dictionary or not.


class Strategy:
methods:
    get_script_data() - gets_script_data
    
    get_signals() - gets signals for fetched script_data
    
    get_lines_to_plot() - extra function to plot indicator and close of that script_data (Strategy with that script should exist.)
    
    
FUNCTIONS:
    indicator1(df) - gets moving avg of 'close' column and stores as "indicator".
    
    find_intersecting_points(df, col_to_compare, col_with_wich_to_compare) - finds indexes of row where "close" and "indicator" intersected.
    
    plot_stock_graph(df) - plots lines of close and indicator columns of dataframe. (dataframe with that script should exist.)
    
    