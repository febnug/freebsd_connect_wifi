<h3>setting, konfigurasi untuk connect wifi di freebsd</h3>
<hr>


<ol>
  <li><p>edit file di <code>/etc/rc.conf</code> tambahin baris ini :</p>
    <p>
      <pre>
wlans_ath0 = "wlan0"
ifconfig_wlan0 = "WPA SYNCDHCP"
      </pre>
</p>
  <p>di save</p>
  </li>
    <li><p>edit file di <code>/etc/wpa_supplicant.conf</code> tambahin baris ini :</p>
    <p>
      <pre>
  ctrl_interface_group = wheel
  network = {
  ssid = "nama_ssid"
  scan_ssid = 1
  psk = "password"
}
      </pre>
      <p>di save</p>
</p>
  </li>
    <li><p>edit file di <code>/etc/resolv.conf</code> tambahin baris ini :</p>
    <p>
      <pre>
search google.com
nameserver 8.8.8.8
      </pre>
      <p>di save</p>
</p>
  </li>
</ol>
