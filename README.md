# gr-iridium-get_IQ_samples

This is a modified version of `gr-iridium` to extract IQ samples from the `burst_downmix` block for satellite authentication.

## Features
- Uses bursts after the RRC filter (`burst_rrc`) in the `burst_downmix` block to extract IQ samples.
- Appends `burst_rrc` to the original burst stream.
- Passes the modified burst stream to the `iridium_qpsk_demod` block for demodulation.
- Successfully demodulated bursts are sent to the `iridium_frame_printer` block and exported to a file along with the demodulated bits.

## Installation & Usage
To use this modified project, you need to:
1. Modify `iridium_frame_printer_impl.cc` in the `lib` directory.
2. Change the IQ file save path to your own directory.
3. Compile and run as per the official `gr-iridium` repository.

For more details, please refer to the official [gr-iridium repository](https://github.com/your-repository-link).

## References
If you need further reference, please check the following paper:  
**"3D Convolution-Based Radio Frequency Fingerprinting for Satellite Authentication"**  
📄 [Read the Paper](https://ieeexplore.ieee.org/document/10436963)

![Project Image](https://github.com/user-attachments/assets/2add6b89-dfcc-40cb-8dce-91ca4ef7a744)
