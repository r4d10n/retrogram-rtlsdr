# retrogram~rtlsdr 

	          _                                      /\/|    _   _ _________________ 
	         | |                                    |/\/    | | | /  ___|  _  \ ___ \
	 _ __ ___| |_ _ __ ___   __ _ _ __ __ _ _ __ ___    _ __| |_| \ `--.| | | | |_/ /
	| '__/ _ \ __| '__/ _ \ / _` | '__/ _` | '_ ` _ \  | '__| __| |`--. \ | | |    / 
	| | |  __/ |_| | | (_) | (_| | | | (_| | | | | | | | |  | |_| /\__/ / |/ /| |\ \ 
	|_|  \___|\__|_|  \___/ \__, |_|  \__,_|_| |_| |_| |_|   \__|_\____/|___/ \_| \_|
	                         __/ |                                                   
	                        |___/                                                    


Wideband Spectrum analyzer on your terminal/ssh console with ASCII art. 
Hacked from Ettus UHD RX ASCII Art DFT code for RTLSDR. Adapted from [retrogram~plutosdr](). 

Pan & Zoom spectrum using keyboard controls [decrement-Increment]. 

* Center Frequency using keys [f-F] 
* Sampling rate    using keys [r-R]
* Gain 			   using keys [g-G]
* Reference level  using keys [l-L] 
* Dynamic Range    using keys [d-D]
* Frame rate       using keys [s-S]
* Tuning step	   using keys [t-T]

Tuning step applies for decrementing / Incrementing Center Frequency and Sampling Rate.

---

## Requires: librtlsdr, libcurses, libboost-program-options
	
	sudo apt install librtlsdr-dev libncurses5-dev libboost-program-options-dev

## Build:

For running on a Linux host with RTLSDR 

	make

## Run:

	./retrogram-rtlsdr --rate 1.8e6 --freq 100e6 --step 1e5

## TODO:

* Generic support for osmosdr devices
* Direct Freq Entry / parameter change 
* Mouse tuning
* Modularize / Optimize with std::vector transform
* Waterfall (!) / Markers / Demodulators (!!) :)
* HTML output / Web(sockets)-server
