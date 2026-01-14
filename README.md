# school-form
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Admission Form — Swami Vivekananda Centenary School (with Plans)</title>
  <meta name="description" content="Admission form as main content plus school plans, schedules and resources." />
  <style>
    /* Base: combine admission form look with a plans panel */
    :root{
      --accent:#2b81f7;
      --muted:#6b7280;
      --card-bg: rgba(255,255,255,0.06);
      --glass: rgba(255,255,255,0.08);
      --radius:14px;
      --max-width:1200px;
      --shadow: 0 10px 35px rgba(0,0,0,0.45);
      font-family: Arial, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", sans-serif;
    }

    html,body{height:100%;margin:0;background:linear-gradient(135deg,#101722 0%, #1b2f47 100%); color:#fff;-webkit-font-smoothing:antialiased}
    .wrap{max-width:var(--max-width);margin:28px auto;padding:20px;box-sizing:border-box;}
    .topbar{display:flex;align-items:center;justify-content:space-between;gap:12px;margin-bottom:18px}
    .brand {display:flex;gap:12px;align-items:center}
    .logo{width:52px;height:52px;background:var(--accent);border-radius:10px;display:inline-flex;align-items:center;justify-content:center;font-weight:800;color:#fff;font-size:18px;box-shadow:0 6px 18px rgba(0,0,0,0.3)}
    .title {font-size:18px;font-weight:800}
    .subtitle {color:#cfe7ff;font-size:13px}

    /* Layout */
    .layout{display:grid;grid-template-columns: 1fr 380px;gap:20px;align-items:start}
    @media(max-width:980px){ .layout{grid-template-columns:1fr} }

    /* Admission container (keeps original look) */
    .admission {
      background: linear-gradient(135deg, rgba(255,255,255,0.04), rgba(255,255,255,0.02));
      padding:28px;border-radius:var(--radius);box-shadow:var(--shadow);min-height:520px;
      border:1px solid rgba(255,255,255,0.04);
    }
    .admission h2 { text-align: center; color: #00e0ff; margin-top:0 }
    .admission label { display:block; margin:10px 0 6px; font-weight:700; color:#dfefff }
    .admission input, .admission textarea, .admission select {
      width:100%; padding:10px; border:none; border-radius:8px; margin-bottom:12px;
      background: rgba(255,255,255,0.06); color:#fff; outline:none; font-size:14px;
    }
    .admission .btn {
      width:100%; padding:12px; background:linear-gradient(90deg,#00c6ff,#0072ff);
      border:none;border-radius:10px;color:#fff;font-weight:800;cursor:pointer;font-size:15px;
    }
    .result { margin-top:18px; text-align:center; font-size:17px; font-weight:700 }
    .success { color:#7ef2b7 }
    .fail { color:#ff9aa2 }

    .details {
      margin-top:16px; background: rgba(255,255,255,0.04); padding:14px; border-radius:10px; color:#fff;
    }
    .details h3 { margin:0 0 8px; color:#ffd966 }

    /* Plans panel */
    .plans {
      background: linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.02));
      padding:18px; border-radius:12px; box-shadow:0 8px 24px rgba(0,0,0,0.32);
      border:1px solid rgba(255,255,255,0.03);
    }
    .plans h3{margin:0 0 8px;color:var(--accent)}
    .plans p.lead{color:#cfe7ff;margin:6px 0 12px;font-size:14px}
    .plan-card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); padding:12px;border-radius:10px;margin-bottom:12px;border:1px solid rgba(255,255,255,0.03)}
    .price{color:var(--accent);font-weight:900}
    .features{color:#dfefff;margin:8px 0 0;padding-left:16px;font-size:13px}
    .plan-cta{margin-top:10px;display:flex;gap:8px}
    .small {font-size:13px;color:#bcd8ff}

    /* Footer note */
    .foot-note{margin-top:14px;color:#bcd8ff;font-size:13px;text-align:center}

    /* Utility */
    a.btn-outline{display:inline-block;padding:8px 12px;border-radius:8px;border:1px solid rgba(255,255,255,0.06);color:#eaf6ff;text-decoration:none;font-weight:700}
  </style>
</head>
<body>
  <div class="wrap">
    <div class="topbar">
      <div class="brand">
        <div class="logo" aria-hidden="true">SVC</div>
        <div>
          <div class="title">Swami Vivekananda Centenary School</div>
          <div class="subtitle">Admission & Plans portal</div>
        </div>
      </div>
      <div style="display:flex;gap:10px;align-items:center">
        <div class="small">Term starts: <strong>2026-02-15</strong></div>
        <a class="btn-outline" href="#plans">See Plans</a>
      </div>
    </div>

    <div class="layout">
      <!-- Main: Admission form (kept structure and ids from your original code) -->
      <main class="admission" role="main" aria-labelledby="admission-title">
        <h2 id="admission-title">Admission Form</h2>
        <form id="admissionForm">
          <label>Your Name:</label>
          <input type="text" id="name" required>

          <label>Your Age:</label>
          <input type="number" id="age" required>

          <label>Your Mother's Name:</label>
          <input type="text" id="mother" required>

          <label>Your Father's Name:</label>
          <input type="text" id="father" required>

          <label>Your Address:</label>
          <textarea id="address" rows="2" required></textarea>

          <label>Your Marital Status:</label>
          <select id="marital" required>
            <option value="">Select...</option>
            <option>Single</option>
            <option>Married</option>
            <option>Other</option>
          </select>

          <label>Your Phone Number:</label>
          <input type="text" id="phone" required>

          <label>Your Email Address:</label>
          <input type="email" id="email" required>

          <label>Advance Admission Fees:</label>
          <input type="number" id="fees" required>
          <p class="small"><strong>Advance Donation is 50000</strong></p>

          <label>Your PIN:</label>
          <input type="password" id="pin" required>

          <label>Your Bank Account Number:</label>
          <input type="text" id="bankAccount" required>

          <label>Select Your Bank:</label>
          <select id="bankName" required>
            <option value="">Select Bank...</option>
            <option>SBI</option><option>HDFC</option><option>ICICI</option>
            <option>Axis Bank</option><option>Punjab National Bank</option>
            <option>Bank of Baroda</option><option>Canara Bank</option>
            <option>Union Bank of India</option><option>IDBI Bank</option>
            <option>Kotak Mahindra Bank</option><option>Yes Bank</option>
          </select>

          <label>Upload Your Photo:</label>
          <input type="file" id="photo" accept="image/*" required>

          <button type="submit" class="btn">Submit</button>
        </form>

        <div id="result" class="result" aria-live="polite"></div>
        <div id="details" class="details" style="display:none;"></div>

        <div class="foot-note">After successful admission, an Excel slip will be generated and a student id card page is prepared (local redirect to idcard.html).</div>
      </main>

      <!-- Right: Plans & Info (added ideas and resources) -->
      <aside class="plans" id="plans" aria-labelledby="plans-heading">
        <h3 id="plans-heading">Plans & Highlights</h3>
        <p class="lead">Flexible, curriculum-aligned plans for preschool, primary and secondary students. Use these plans to inform parents during admission.</p>

        <div class="plan-card" aria-hidden="false">
          <strong>Preschool Plan</strong>
          <div class="price small">Free trial • Contact for pricing</div>
          <p class="small">Play-based learning, early literacy and numeracy — ideal for ages 3–5.</p>
          <ul class="features">
            <li>Morning circle & sensory activities</li>
            <li>Weekly learning objectives & theme-based units</li>
            <li>Parent update reports & milestone tracker</li>
          </ul>
          <div class="plan-cta">
            <a class="btn-outline" href="#contact">Enroll or ask</a>
          </div>
        </div>

        <div class="plan-card">
          <strong>Primary School Plan</strong>
          <div class="price">$120 / month</div>
          <p class="small">Structured lessons across literacy, numeracy, science, and arts for ages 6–11.</p>
          <ul class="features">
            <li>Daily lesson plans & homework templates</li>
            <li>Assessment checklists & parent-teacher notes</li>
            <li>After-school clubs and extracurricular suggestions</li>
          </ul>
          <div class="plan-cta">
            <a class="btn-outline" href="#contact">Request schedule</a>
          </div>
        </div>

        <div class="plan-card">
          <strong>Secondary School Plan</strong>
          <div class="price">$180 / month</div>
          <p class="small">Exam-focused timetables, subject trackers, and college guidance for ages 12–18.</p>
          <ul class="features">
            <li>Weekly revision timetables & subject trackers</li>
            <li>Exam practice schedules & resource packs</li>
            <li>Career counseling & college preparation guidance</li>
          </ul>
          <div class="plan-cta">
            <a class="btn-outline" href="#contact">Get details</a>
          </div>
        </div>

        <div style="margin-top:12px" class="small">
          Quick tips:
          <ul style="margin:8px 0 0 18px">
            <li>Customize schedules to local term dates.</li>
            <li>Share PDF plans with parents (Print → Save as PDF).</li>
            <li>Keep photos and logos updated in your resources.</li>
          </ul>
        </div>

        <div style="margin-top:14px">
          <strong>Contact</strong>
          <p class="small">Phone: <strong>+1 555-555-5555</strong></p>
          <p class="small">Email: <strong><a href="mailto:info@example.com" style="color:#cfe7ff">info@example.com</a></strong></p>
        </div>
      </aside>
    </div>
  </div>

  <!-- SheetJS for Excel (kept from original) -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>

  <script>
    // --- Admission form behavior (original logic preserved, integrated) ---
    document.getElementById("admissionForm").addEventListener("submit", function(e) {
      e.preventDefault();

      let name = document.getElementById("name").value;
      let age = document.getElementById("age").value;
      let mother = document.getElementById("mother").value;
      let father = document.getElementById("father").value;
      let address = document.getElementById("address").value;
      let marital = document.getElementById("marital").value;
      let phone = document.getElementById("phone").value;
      let email = document.getElementById("email").value;
      let fees = parseInt(document.getElementById("fees").value);
      let pin = document.getElementById("pin").value;
      let bankAccount = document.getElementById("bankAccount").value;
      let bankName = document.getElementById("bankName").value;
      let photoFile = document.getElementById("photo").files[0];

      let result = document.getElementById("result");
      let details = document.getElementById("details");

      let reason = "";
      let success = false;

      if (pin === "12345" && fees === 50000) {
        success = true;
        result.textContent = "ADMISSION COMPLETED";
        result.className = "result success";

        // Generate Excel Slip
        const slipData = [
          ["Admission Slip"],
          ["Name", name],
          ["Age", age],
          ["Mother's Name", mother],
          ["Father's Name", father],
          ["Address", address],
          ["Marital Status", marital],
          ["Phone", phone],
          ["Email", email],
          ["Fees Paid", fees],
          ["Bank Account", bankAccount],
          ["Bank Name", bankName],
          ["Date", new Date().toLocaleDateString()]
        ];
        const ws = XLSX.utils.aoa_to_sheet(slipData);
        const wb = XLSX.utils.book_new();
        XLSX.utils.book_append_sheet(wb, ws, "Slip");
        XLSX.writeFile(wb, "AdmissionSlip.xlsx");

        // Save photo + details and redirect
        if (photoFile) {
          const reader = new FileReader();
          reader.onload = function(event) {
            try {
              localStorage.setItem("studentData", JSON.stringify({
                name, age, mother, father, address, marital,
                phone, email, fees, bankAccount, bankName, photo: event.target.result
              }));
            } catch (err) {
              // localStorage may fail if storage is full; ignore for demo
              console.warn('Could not save to localStorage:', err);
            }
            // Redirect to idcard.html (user should provide this file)
            window.location.href = "idcard.html";
          };
          reader.readAsDataURL(photoFile);
        } else {
          // No photo (shouldn't happen because input is required) — still redirect
          window.location.href = "idcard.html";
        }

      } else {
        if (pin !== "12345" && fees !== 50000) {
          reason = "Invalid PIN and Fees amount.";
        } else if (pin !== "12345") {
          reason = "Invalid PIN entered.";
        } else if (fees !== 50000) {
          reason = "Fees must be exactly 50000.";
        }
        result.textContent = "ADMISSION FAILED";
        result.className = "result fail";
        details.style.display = "block";
        details.innerHTML = `<h3>Admission Slip</h3>
          <p><strong>Name:</strong> ${escapeHtml(name)}</p>
          <p style="color:#ff9aa2;"><strong>Reason for Failure:</strong> ${escapeHtml(reason)}</p>`;
      }
    });

    // Small helper to escape basic HTML used in failure details
    function escapeHtml(str){
      if (!str) return '';
      return str.replace(/[&<>"'`=\/]/g, function(s) {
        return ({
          '&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;','`':'&#96;','=':'&#61;','/':'&#47;'
        })[s];
      });
    }

    // (Optional) Smooth focus for accessibility: focus first input on load
    window.addEventListener('load', function(){ const f = document.getElementById('name'); if(f) f.focus(); });
  </script>
</body>
</html>
