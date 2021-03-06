# chi-to-json
Extract data from an eldo .chi file and save it in json format.

## Installation

- Git clone this repository
- `pip install -e <path to this repository>`

## Usage

Run your Eldo simulation as usual (`eldo <your spice netlist>`) and save the `.chi` output file.

Please note that for this program to be able to extract anything you will need to print at least one signal in your netlist with the `.print` command.

If you want more than one signal to be extracted to the same pair of axes, you have to include them in the same `.print` command, i.e. `print V(N_1) V(N_2)` willl use the same plot, whereas `.print V(N_1)` followed by `.print V(N_2)` on the following line will use two separate windows.

Run `chi_to_json <path to your .chi file> <path to desired .json output file>` and wait for the extraction to be finished.

## Supported analyses
- tran
- dc
- ac

## Related repos

If you find this repo useful, there's a good chance you may want to check some of my other related work as well.

- [tannner_to_eldo](https://github.com/ftorres16/tanner_to_eldo) can transform Tanner generated SPICE netlists into ELDO compatible ones.
- [plot_eldo_sims](https://github.com/ftorres16/plot_eldo_sims) can plot the JSON output of this command using Python's matlplotlib.
