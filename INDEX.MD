<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Inspectors Group Inspection Report</title>
    <style>
        @import url('https://themes.googleusercontent.com/fonts/css?kit=vTbT7urhBWoQfR2Ssl4_0CmRZpIX9SNBjLkdcpGW6dk');

        body {
            background-color: #ffffff;
            max-width: 100%;
            padding: 16px;
            font-family: 'Arial', sans-serif;
            font-size: 11pt;
            color: #000000;
            box-sizing: border-box;
        }

        .title {
            text-align: center;
            font-family: 'Oswald', sans-serif;
            font-size: 26pt;
            color: #0000ff;
            font-weight: 700;
            margin-bottom: 20px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }

        td, th {
            padding: 5pt;
            border: 1pt solid #000000;
            vertical-align: top;
        }

        th {
            background-color: #f0f0f0;
            font-weight: 700;
        }

        .section-title {
            text-align: left;
            font-size: 15pt;
            color: #000000;
            font-weight: 700;
            font-family: 'Oswald', sans-serif;
            margin-top: 20px;
        }

        .text-center {
            text-align: center;
        }

        #image-list img {
            max-width: 100px;
            height: auto;
            margin-top: 10px;
            cursor: pointer;
        }

        .button-container {
            margin-top: 20px;
        }

        .button-container button {
            margin-right: 10px;
        }

        .dollar-input {
            color: red;
            font-weight: bold;
        }

        .description {
            margin-top: 5px;
            width: calc(100% - 12px);
            box-sizing: border-box;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            padding-top: 60px;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgb(0, 0, 0);
            background-color: rgba(0, 0, 0, 0.9);
        }

        .modal-content {
            margin: auto;
            display: block;
            width: 80%;
            max-width: 700px;
        }

        .close {
            position: absolute;
            top: 15px;
            right: 35px;
            color: #f1f1f1;
            font-size: 40px;
            font-weight: bold;
            transition: 0.3s;
        }

        .close:hover,
        .close:focus {
            color: #bbb;
            text-decoration: none;
            cursor: pointer;
        }

        .download-link {
            display: none;
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>

<body>
    <div class="title">THE INSPECTORS GROUP INSPECTION REPORT</div>

    <div style="margin-bottom: 20px;">
        CLAIM NUMBER: <input type="text" id="claim-number">
    </div>

    <table>
        <tr>
            <td>VERBAL REPORT TO: <input type="text" id="verbal-report-to"></td>
            <td>MILEAGE: <input type="text" id="mileage"></td>
            <td>PRODUCTION DATE: <input type="text" id="production-date"></td>
        </tr>
        <tr>
            <td>DATE ON RO: <input type="text" id="date-on-ro"></td>
            <td>VIN #: <input type="text" id="vin-number"></td>
            <td>LABOR RATE: <input type="text" id="labor-rate"></td>
        </tr>
        <tr>
            <td>RO NUMBER: <input type="text" id="ro-number"></td>
            <td>LICENSE PLATE: <input type="text" id="license-plate"></td>
            <td>LABOR PROVIDED: 
                <select id="labor-provided">
                    <option value="">SELECT ONE</option>
                    <option value="Posted">Posted</option>
                    <option value="Verbal">Verbal</option>
                </select>
            </td>
        </tr>
        <tr>
            <td>RO NAME: <input type="text" id="ro-name"></td>
            <td>STATE: 
                <select id="state">
                    <option value="AL">AL</option>
                    <option value="AK">AK</option>
                    <option value="AZ">AZ</option>
                    <option value="AR">AR</option>
                    <option value="CA">CA</option>
                    <option value="CO">CO</option>
                    <option value="CT">CT</option>
                    <option value="DE">DE</option>
                    <option value="FL">FL</option>
                    <option value="GA">GA</option>
                    <option value="HI">HI</option>
                    <option value="ID">ID</option>
                    <option value="IL">IL</option>
                    <option value="IN">IN</option>
                    <option value="IA">IA</option>
                    <option value="KS">KS</option>
                    <option value="KY">KY</option>
                    <option value="LA">LA</option>
                    <option value="ME">ME</option>
                    <option value="MD">MD</option>
                    <option value="MA">MA</option>
                    <option value="MI">MI</option>
                    <option value="MN">MN</option>
                    <option value="MS">MS</option>
                    <option value="MO">MO</option>
                    <option value="MT">MT</option>
                    <option value="NE">NE</option>
                    <option value="NV">NV</option>
                    <option value="NH">NH</option>
                    <option value="NJ">NJ</option>
                    <option value="NM">NM</option>
                    <option value="NY">NY</option>
                    <option value="NC">NC</option>
                    <option value="ND">ND</option>
                    <option value="OH">OH</option>
                    <option value="OK">OK</option>
                    <option value="OR">OR</option>
                    <option value="PA">PA</option>
                    <option value="RI">RI</option>
                    <option value="SC">SC</option>
                    <option value="SD">SD</option>
                    <option value="TN">TN</option>
                    <option value="TX">TX</option>
                    <option value="UT">UT</option>
                    <option value="VT">VT</option>
                    <option value="VA">VA</option>
                    <option value="WA">WA</option>
                    <option value="WV">WV</option>
                    <option value="WI">WI</option>
                    <option value="WY">WY</option>
                </select>
            </td>
            <td>TOWED/DRIVEN: 
                <select id="towed-driven">
                    <option value="">SELECT ONE</option>
                    <option value="Towed">Towed</option>
                    <option value="Driven">Driven</option>
                </select>
            </td>
        </tr>
    </table>

    <div class="section-title">CUSTOMER COMPLAINT ON RO:</div>
    <table>
        <tr>
            <td><textarea rows="4" cols="50" id="customer-complaint"></textarea></td>
        </tr>
    </table>

    <table>
        <tr>
            <th class="text-center">FLUID</th>
            <th class="text-center">LEVEL</th>
            <th class="text-center">CONDITION</th>
        </tr>
        <tr>
            <td class="text-center">ENGINE OIL</td>
            <td class="text-center">
                <select id="engine-oil-level">
                    <option value="">SELECT ONE</option>
                    <option value="Full">Full</option>
                    <option value="Low">Low</option>
                    <option value="Drained">Drained</option>
                    <option value="Empty">Empty</option>
                    <option value="Overfull">Overfull</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
            <td class="text-center">
                <select id="engine-oil-condition">
                    <option value="">SELECT ONE</option>
                    <option value="Good">Good</option>
                    <option value="Fair">Fair</option>
                    <option value="Poor">Poor</option>
                    <option value="Burnt">Burnt</option>
                    <option value="Intermixed">Intermixed</option>
                    <option value="Contaminated">Contaminated</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
        </tr>
        <tr>
            <td class="text-center">TRANSMISSIONS</td>
            <td class="text-center">
                <select id="transmissions-level">
                    <option value="">SELECT ONE</option>
                    <option value="Full">Full</option>
                    <option value="Low">Low</option>
                    <option value="Drained">Drained</option>
                    <option value="Empty">Empty</option>
                    <option value="Overfull">Overfull</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
            <td class="text-center">
                <select id="transmissions-condition">
                    <option value="">SELECT ONE</option>
                    <option value="Good">Good</option>
                    <option value="Fair">Fair</option>
                    <option value="Poor">Poor</option>
                    <option value="Burnt">Burnt</option>
                    <option value="Intermixed">Intermixed</option>
                    <option value="Contaminated">Contaminated</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
        </tr>
        <tr>
            <td class="text-center">COOLANT</td>
            <td class="text-center">
                <select id="coolant-level">
                    <option value="">SELECT ONE</option>
                    <option value="Full">Full</option>
                    <option value="Low">Low</option>
                    <option value="Drained">Drained</option>
                    <option value="Empty">Empty</option>
                    <option value="Overfull">Overfull</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
            <td class="text-center">
                <select id="coolant-condition">
                    <option value="">SELECT ONE</option>
                    <option value="Good">Good</option>
                    <option value="Fair">Fair</option>
                    <option value="Poor">Poor</option>
                    <option value="Burnt">Burnt</option>
                    <option value="Intermixed">Intermixed</option>
                    <option value="Contaminated">Contaminated</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
        </tr>
        <tr>
            <td class="text-center">RADIATOR</td>
            <td class="text-center">
                <select id="radiator-level">
                    <option value="">SELECT ONE</option>
                    <option value="Full">Full</option>
                    <option value="Low">Low</option>
                    <option value="Drained">Drained</option>
                    <option value="Empty">Empty</option>
                    <option value="Overfull">Overfull</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
            <td class="text-center">
                <select id="radiator-condition">
                    <option value="">SELECT ONE</option>
                    <option value="Good">Good</option>
                    <option value="Fair">Fair</option>
                    <option value="Poor">Poor</option>
                    <option value="Burnt">Burnt</option>
                    <option value="Intermixed">Intermixed</option>
                    <option value="Contaminated">Contaminated</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
        </tr>
        <tr>
            <td class="text-center">TRANSFER CASE</td>
            <td class="text-center">
                <select id="transfer-case-level">
                    <option value="">SELECT ONE</option>
                    <option value="Full">Full</option>
                    <option value="Low">Low</option>
                    <option value="Drained">Drained</option>
                    <option value="Empty">Empty</option>
                    <option value="Overfull">Overfull</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
            <td class="text-center">
                <select id="transfer-case-condition">
                    <option value="">SELECT ONE</option>
                    <option value="Good">Good</option>
                    <option value="Fair">Fair</option>
                    <option value="Poor">Poor</option>
                    <option value="Burnt">Burnt</option>
                    <option value="Intermixed">Intermixed</option>
                    <option value="Contaminated">Contaminated</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
        </tr>
        <tr>
            <td class="text-center">POWER STEERING</td>
            <td class="text-center">
                <select id="power-steering-level">
                    <option value="">SELECT ONE</option>
                    <option value="Full">Full</option>
                    <option value="Low">Low</option>
                    <option value="Drained">Drained</option>
                    <option value="Empty">Empty</option>
                    <option value="Overfull">Overfull</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
            <td class="text-center">
                <select id="power-steering-condition">
                    <option value="">SELECT ONE</option>
                    <option value="Good">Good</option>
                    <option value="Fair">Fair</option>
                    <option value="Poor">Poor</option>
                    <option value="Burnt">Burnt</option>
                    <option value="Intermixed">Intermixed</option>
                    <option value="Contaminated">Contaminated</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
        </tr>
        <tr>
            <td class="text-center">FRONT DIFF</td>
            <td class="text-center">
                <select id="front-diff-level">
                    <option value="">SELECT ONE</option>
                    <option value="Full">Full</option>
                    <option value="Low">Low</option>
                    <option value="Drained">Drained</option>
                    <option value="Empty">Empty</option>
                    <option value="Overfull">Overfull</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
            <td class="text-center">
                <select id="front-diff-condition">
                    <option value="">SELECT ONE</option>
                    <option value="Good">Good</option>
                    <option value="Fair">Fair</option>
                    <option value="Poor">Poor</option>
                    <option value="Burnt">Burnt</option>
                    <option value="Intermixed">Intermixed</option>
                    <option value="Contaminated">Contaminated</option>
                      <option value="NA">N/A</option>
                </select>
            </td>
        </tr>
        <tr>
            <td class="text-center">REAR DIFF</td>
            <td class="text-center">
                <select id="rear-diff-level">
                    <option value="">SELECT ONE</option>
                    <option value="Full">Full</option>
                    <option value="Low">Low</option>
                    <option value="Drained">Drained</option>
                    <option value="Empty">Empty</option>
                    <option value="Overfull">Overfull</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
            <td class="text-center">
                <select id="rear-diff-condition">
                    <option value="">SELECT ONE</option>
                    <option value="Good">Good</option>
                    <option value="Fair">Fair</option>
                    <option value="Poor">Poor</option>
                    <option value="Burnt">Burnt</option>
                    <option value="Intermixed">Intermixed</option>
                    <option value="Contaminated">Contaminated</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
        </tr>
        <tr>
            <td class="text-center">BRAKE FLUID</td>
            <td class="text-center">
                <select id="brake-fluid-level">
                    <option value="">SELECT ONE</option>
                    <option value="Full">Full</option>
                    <option value="Low">Low</option>
                    <option value="Drained">Drained</option>
                    <option value="Empty">Empty</option>
                    <option value="Overfull">Overfull</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
            <td class="text-center">
                <select id="brake-fluid-condition">
                    <option value="">SELECT ONE</option>
                    <option value="Good">Good</option>
                    <option value="Fair">Fair</option>
                    <option value="Poor">Poor</option>
                    <option value="Burnt">Burnt</option>
                    <option value="Intermixed">Intermixed</option>
                    <option value="Contaminated">Contaminated</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
        </tr>
    </table>

    <table>
        <tr>
            <td>ENGINE TYPE: <input type="text" id="engine-type"></td>
            <td>TRANSMISSION TYPE: <input type="text" id="transmission-type"></td>
            <td>DRIVE TYPE:
                <select id="drive-type">
                    <option value="">SELECT ONE</option>
                    <option value="4WD">4WD</option>
                    <option value="AWD">AWD</option>
                    <option value="FWD">FWD</option>
                    <option value="RWD">RWD</option>
                    <option value="NA">N/A</option>
                </select>
            </td>
        </tr>
    </table>

    <table>
        <tr>
            <td>SERVICE STICKER: <input type="text" id="service-sticker"></td>
            <td>SERVICE HISTORY AT SHOP: <input type="text" id="service-history"></td>
        </tr>
    </table>

    <table>
        <tr>
            <td>COMMERCIAL USE? 
                <select id="commercial-use">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
            <td>EVIDENCE OF TOWING? 
                <select id="evidence-towing">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
            <td>DISCOLORATION? 
                <select id="discoloration">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
        </tr>
        <tr>
            <td>MODIFICATIONS? 
                <select id="modifications">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
            <td>SLUDGE VARNISH? 
                <select id="sludge-varnish">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
            <td>OPERATOR PROTECT VEHICLE? 
                <select id="operator-protect">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
        </tr>
        <tr>
            <td>ABUSE? 
                <select id="abuse">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
            <td>SIGNS OF OVERHEAT? 
                <select id="signs-overheat">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
            <td>ANY PRE-EXISTING CONDITIONS? 
                <select id="pre-existing-conditions">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
        </tr>
        <tr>
            <td>SIGNS OF COLLISION? 
                <select id="signs-collision">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
            <td>LACK OF LUBE? 
                <select id="lack-of-lube">
                    <option value="">SELECT ONE</option>
                    <option value="Yes">Yes</option>
                    <option value="No">No</option>
                </select>
            </td>
            <td>LEVEL OF TEAR DOWN? 
                <textarea rows="4" cols="50" id="tear-down-level"></textarea>
            </td>
        </tr>
    </table>

    <table>
        <tr>
            <td>CURRENT TIRE SIZE: <input type="text" id="current-tire-size"></td>
        </tr>
        <tr>
            <td>FACTORY TIRE SIZE: <input type="text" id="factory-tire-size"></td>
        </tr>
        <tr>
            <td>TIRE TREAD DEPTH: <input type="text" id="tire-tread-depth"></td>
        </tr>
    </table>

    <div class="section-title">REPORT:</div>
    <table>
        <tr>
            <td><textarea rows="4" cols="50" id="report"></textarea></td>
        </tr>
    </table>

    <div class="section-title">CAUSE OF FAILURE:</div>
    <table>
        <tr>
            <td><textarea rows="4" cols="50" id="cause-of-failure"></textarea></td>
        </tr>
    </table>

    <div class="section-title">OPINION OF REPAIRS:</div>
    <table>
        <tr>
            <td><textarea rows="4" cols="50" id="opinion-of-repairs"></textarea></td>
        </tr>
    </table>

    <div class="section-title">UPLOAD IMAGES:</div>
    <input type="file" id="image-uploader" multiple>
    <div id="image-list"></div>

    <div style="margin-top: 20px; font-weight: bold;">
        INSPECTION FEE: $<input type="text" class="dollar-input" id="inspection-fee">
    </div>

    <div class="button-container">
        <button type="button" onclick="saveReport()">Save</button>
        <button type="button" onclick="submitReport()">Submit</button>
    </div>

    <div id="imageModal" class="modal">
        <span class="close" onclick="document.getElementById('imageModal').style.display='none'">&times;</span>
        <img class="modal-content" id="img01">
    </div>

    <a id="download-link" class="download-link" href="#" download="inspection_report.pdf">Download PDF</a>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.4.0/jspdf.umd.min.js"></script>
    <script src="https://html2canvas.hertzen.com/dist/html2canvas.min.js"></script>
    <script>
        document.getElementById('image-uploader').addEventListener('change', function(event) {
            const imageList = document.getElementById('image-list');
            imageList.innerHTML = '';
            const files = event.target.files;
            for (const file of files) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const div = document.createElement('div');
                    const img = document.createElement('img');
                    img.src = e.target.result;
                    img.onclick = function() {
                        document.getElementById('imageModal').style.display = 'block';
                        document.getElementById('img01').src = this.src;
                    };
                    const textarea = document.createElement('textarea');
                    textarea.classList.add('description');
                    textarea.rows = 2;
                    textarea.cols = 50;
                    textarea.placeholder = 'Enter image description here...';
                    div.appendChild(img);
                    div.appendChild(textarea);
                    imageList.appendChild(div);
                };
                reader.readAsDataURL(file);
            }
        });

        async function saveReport() {
            const { jsPDF } = window.jspdf;
            const doc = new jsPDF();

            const content = document.body;
            await html2canvas(content).then(canvas => {
                const imgData = canvas.toDataURL('image/png');
                const imgWidth = 210;
                const pageHeight = 295;
                const imgHeight = canvas.height * imgWidth / canvas.width;
                let heightLeft = imgHeight;
                let position = 0;

                doc.addImage(imgData, 'PNG', 0, position, imgWidth, imgHeight);
                heightLeft -= pageHeight;

                while (heightLeft >= 0) {
                    position = heightLeft - imgHeight;
                    doc.addPage();
                    doc.addImage(imgData, 'PNG', 0, position, imgWidth, imgHeight);
                    heightLeft -= pageHeight;
                }
            });

            const pdfData = doc.output('blob');
            const pdfUrl = URL.createObjectURL(pdfData);

            const downloadLink = document.getElementById('download-link');
            downloadLink.href = pdfUrl;
            downloadLink.style.display = 'block';
        }

        async function submitReport() {
            const { jsPDF } = window.jspdf;
            const doc = new jsPDF();

            const content = document.body;
            await html2canvas(content).then(canvas => {
                const imgData = canvas.toDataURL('image/png');
                const imgWidth = 210;
                const pageHeight = 295;
                const imgHeight = canvas.height * imgWidth / canvas.width;
                let heightLeft = imgHeight;
                let position = 0;

                doc.addImage(imgData, 'PNG', 0, position, imgWidth, imgHeight);
                heightLeft -= pageHeight;

                while (heightLeft >= 0) {
                    position = heightLeft - imgHeight;
                    doc.addPage();
                    doc.addImage(imgData, 'PNG', 0, position, imgWidth, imgHeight);
                    heightLeft -= pageHeight;
                }
            });

            const pdfData = doc.output('blob');

            const email = 'theinspectorsgroup@yahoo.com';
            const subject = 'Inspection Report';
            const body = 'Please find attached the inspection report.';
            const mailtoLink = `mailto:${email}?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;

            const a = document.createElement('a');
            a.href = URL.createObjectURL(pdfData);
            a.download = 'inspection_report.pdf';
            a.click();

            window.location.href = mailtoLink;
        }
    </script>
</body>

</html>


                
